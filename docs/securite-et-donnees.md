# Sécurité et protection des données

**Statut : conception, pas implémentation.** Rien de ce qui suit n’existe dans le prototype, qui ne se connecte à rien et ne garde aucune donnée. Ce sont des engagements de conception, présentés pendant le travail dans un bloc de diapositives (version Chronos, [archivées](../archives/chronos-presentation-tour-de-controle.html)) puis retirés du pitch final, pour un jury de juristes, au profit d’une seule diapositive technique facultative. Toutes les valeurs (algorithmes, délais, matrice des droits) sont indicatives et à valider avec des juristes, le délégué à la protection des données et le ministère.

## Les quatre contraintes du hackathon

Elles viennent du cadre du sujet, citées dans une note de conception collée par l’équipe, qui les a confirmées le 16 octobre 2026.

| Contrainte | Réponse de Kairos |
|---|---|
| Validation humaine avant toute modification | Kairos propose, un agent du greffe valide chaque envoi d’un clic. L’IA ne décide, ne note et ne qualifie rien. Aucune décision fondée sur un traitement automatisé (article 22 du RGPD, article 47 de la loi Informatique et libertés ; données pénales : directive (UE) 2016/680) |
| Journalisation des accès et des modifications | Chaque consultation, validation, envoi et accusé de réception est inscrit au journal avec l’auteur, l’heure, le motif et la source. Le prototype montre ce journal |
| Protection des données des justiciables | Voir ci-dessous |
| Standards d’échange ouverts | API documentées entre services, formats structurés (JSON ou XML), identifiant commun de dossier et d’événement, avec la source, l’auteur et la version de chaque donnée conservés. « Une donnée saisie une fois, tracée partout » |

## Principe directeur

Kairos relie les données, il ne les copie pas. Il garde des références, des identifiants pseudonymes, les projets de messages et un journal, qui sont eux-mêmes des données personnelles et demandent le même niveau d’exigence que leur source.

## Six risques, six réponses

| Risque | Réponse envisagée |
|---|---|
| Une base centrale qui fuit | Pas de copie des dossiers : des liens et des identifiants pseudonymes, les données restent dans les applications sources |
| Un disque ou une sauvegarde volés | Chiffrement au repos (AES-256) et en transit (TLS 1.3), sauvegardes chiffrées |
| Un administrateur ou l’hébergeur qui lit les données | Clés détenues par le ministère dans un module matériel (HSM). Aucun accès administrateur permanent : accès à la demande, validé à deux, tracé |
| L’adresse d’une victime exposée | Champ chiffré à part, masqué par défaut, affiché seulement au profil habilité, après réauthentification et avec un motif |
| Des données gardées trop longtemps | Purge automatique à la clôture du dossier et à l’échéance légale de conservation |
| Un hébergement hors de contrôle | Hébergement en France sur un cloud de confiance qualifié SecNumCloud, à arrêter avec le ministère ; modèle d’IA hébergé dans l’environnement du ministère et jamais entraîné sur les données, sous contrat de sous-traitance |

## Qui voit quoi

Matrice indicative, à écrire avec les juristes et le ministère. Principe : droits par rôle, par dossier et par motif ; aucun accès par défaut ; tout accès « sur motif » est justifié et tracé. La plateforme voit en croisé, chaque utilisateur ne voit que sa part.

| | Décision | Mesures de protection | Adresse protégée | Dossier pénal | Dossier des enfants |
|---|---|---|---|---|---|
| Greffe du service | oui | oui | sur motif | non | non |
| Parquet | oui | oui | sur motif | oui | sur motif |
| JAP et SPIP | oui | oui | sur motif | oui | non |
| Police et gendarmerie | oui | oui | non | non | non |
| Avocat de la victime | oui | oui | oui | non | non |
| Avocat de l’auteur | oui | oui | jamais | non | non |
| Victime | message clair | oui | non | non | non |

## Double authentification, adaptée à chacun

| Profil | Authentification | Périmètre |
|---|---|---|
| Magistrat, greffier | Carte agent ou clé de sécurité FIDO2, plus code PIN, sur poste professionnel géré | Les dossiers de son service |
| Police, gendarmerie, SPIP | Identité de leur administration (fédérée), plus un second facteur physique | Les mesures à appliquer, rien d’autre |
| Avocat | Clé RPVA ou carte professionnelle, plus code | Les dossiers de ses clients |
| Victime | FranceConnect+ ou code à usage unique par application ; **par défaut, l’information passe par son avocate** | Les messages validés qui la concernent |

Règles communes : réauthentification avant toute validation ou donnée protégée ; accès conditionnel (appareil géré, lieu et horaire vérifiés) ; sessions courtes et verrouillage automatique ; connexion inhabituelle bloquée et signalée ; droits retirés dès le départ d’un agent ; aucune donnée sensible dans les notifications externes (« une information est disponible dans votre espace sécurisé »).

## Traçabilité et IA sous contrôle

- **Journal** horodaté, en écriture seule, entrées chaînées, accès restreints, durée de conservation fixée. Il contient lui-même des données sensibles ; on ne parle pas de journal « inviolable ».
- **Détection des abus** : un agent qui consulte un dossier hors de son service, une adresse protégée ou un volume inhabituel déclenche une alerte de sécurité. Réaction : compte suspendu, responsable de la sécurité alerté, notification à la CNIL sous 72 heures en cas de violation.
- **IA** : elle lit et propose, sans aucun droit d’envoi ni de modification. Le texte d’un document lu est une donnée, jamais une instruction (un document piégé ne commande rien). Pas de source, pas d’alerte : chaque fait renvoie à l’acte d’origine. Rien ne part sans validation humaine.
- **Pas de note, pas de classement** de personnes, d’affaires ni d’agents. Les indicateurs sont agrégés par service ou par type de décision, jamais par agent.

## Accès sur tous les appareils, standards

Application web adaptée à chaque écran plutôt qu’applications séparées ; aucune donnée persistante sur l’appareil (pas de téléchargement par défaut, pas de cache sensible) ; notifications neutres sur mobile (« 1 action en attente ») ; verrouillage et déconnexion automatiques, appareil révocable à distance ; même moteur de droits partout. Échanges entre services par une passerelle d’API unique, authentification mutuelle des services, jetons à portée limitée, messages signés et horodatés avec accusé de réception.

## Avant un pilote

Analyse d’impact sur la protection des données (AIPD) avec le délégué à la protection des données ; avis de la CNIL (données pénales et données de victimes) ; homologation de sécurité selon le référentiel général de sécurité (RGS) ; test d’intrusion par un prestataire qualifié, avant ouverture puis chaque année ; revue des droits chaque trimestre et exercices de reprise. Kairos n’est pas sur le chemin critique : s’il s’arrête, les services retrouvent leurs circuits habituels (plan de reprise testé, sauvegardes dans une seconde région en France).

## Ce que nous avons remis en question

La note de conception d’origine ([texte](../archives/textes-d-origine/05-conception-securite-interservices.md)) a été relue de façon critique avant d’être reprise :

- **La victime est le point le plus sensible.** Une double authentification par code ou application devient un danger si l’auteur a accès à son téléphone, à son courriel ou à son logement. Pas d’accès direct par défaut : l’information passe par son avocate ou par un canal qu’elle choisit. Même une notification « neutre » peut trahir quelque chose sur un téléphone partagé. C’est la même logique que la remarque de l’expert : un message mal envoyé peut être plus dangereux qu’un message absent.
- **« Charge par agent »** : contraire à « Kairos n’évalue aucune personne ». On compte par service et par file d’actions.
- **« L’agent des enfants ne voit pas le pénal »** : Kairos relie justement pénal, famille et enfants. Le bon principe est la vue croisée pour la plateforme, la vue limitée pour chaque utilisateur.
- **Les réquisitions** (hub d’échange pour les demandes aux tiers) : un autre produit, qui relève de l’enquête et non de la circulation d’une décision, avec un cadre légal à établir. Kairos n’en émet aucune.
- **« Pas de base dupliquée » et « journal inviolable »** : promesses trop fortes, reformulées ci-dessus.
- **« Sécurité totale »** : à ne jamais promettre. On promet le moindre privilège, la traçabilité, le chiffrement, la reprise.
- **Appareils personnels** : incompatibles, à notre connaissance, avec ce qu’acceptent les administrations de la justice ; appareils professionnels gérés seulement, à valider avec la DSI.
- **Alerte de connexion inhabituelle et statistiques par agent** : peuvent exiger l’information ou la consultation des représentants du personnel, à vérifier.
- **Où l’IA lit les actes pénaux**, il faut dire où les données sont traitées, avec une exigence de type SecNumCloud, sans entraînement sur les données ; non vérifié pour la justice française.

## Cadre juridique cité dans le projet

Article 48-1 et articles R. 15-33-66-4 et suivants du code de procédure pénale (Cassiopée) ; délibération CNIL n° 2009-170 du 26 mars 2009 ; règlement (UE) 2016/679, article 22 ; loi n° 78-17 du 6 janvier 1978, article 47 ; directive (UE) 2016/680 (données pénales) ; règlement européen sur l’IA, dont l’annexe III (usages à haut risque dans le domaine de la justice) est à qualifier avec des juristes : l’argument est que Kairos reste dans la préparation administrative et la notification, sans appréciation juridique. Pour les pistes explorées puis écartées : article 230-19 du CPP (fichier des personnes recherchées), articles 706-53-1 et suivants (FIJAIS), articles 230-20 et suivants (logiciels de rapprochement) ; voir [les pistes](pistes-explorees.md).
