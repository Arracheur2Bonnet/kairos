# Questions attendues et réponses

Les réponses viennent des annexes des présentations et de nos préparations. Celles qui n’ont pas de réponse arrêtée sont dans la dernière partie : mieux vaut le dire que de l’improviser.

## Sur le fonctionnement

**Comment savoir que le message est lu ?** Le message contient un lien sécurisé : « lu » signifie que le lien a été ouvert. C’est pourquoi le pitch dit « consulté quand c’est techniquement possible ». Un SMS ne donne pas d’accusé de lecture fiable. Sans ouverture à temps, le greffe appelle.

**Et si la victime a changé de numéro, de domicile, d’avocat ?** Chaque coordonnée est conservée avec sa date et sa source. Kairos ne devine jamais : le téléphone est privilégié et, au moindre doute, une confirmation est demandée (par l’avocate ou le commissariat) avant tout envoi. C’est l’avertissement de notre mentor, avocat, le 15 octobre : un message mal envoyé peut être plus dangereux qu’un message absent.

**Et si l’IA se trompe ?** Elle ne décide rien. Chaque alerte et chaque fait cite l’acte d’origine et se vérifie à la source, en un clic. Chaque envoi est validé par un agent du greffe.

**Qui est responsable de l’envoi ?** Le greffe : Kairos rédige, l’agent valide, l’envoi part ensuite, tracé au journal.

**Quelle différence avec un tableau de bord ?** L’IA lit les actes et explique, adresse chaque alerte au bon service, envoie après validation et prouve la réception. Un tableau de bord affiche, il ne vérifie ni ne prévient.

**Pourquoi pas une évolution de Cassiopée ?** Kairos la complète : il prolonge sa mission d’information (article 48-1 du CPP) au-delà de ses murs et en apporte la preuve, sans rien remplacer. Cassiopée ne voit pas les autres logiciels et ne sait pas si la victime a reçu l’information.

**Et SISPoPP ?** Il est peu utilisé parce qu’il faut tout y ressaisir (constat de l’IGJ). Kairos part du principe inverse : une information saisie une fois devient connue de tous ceux qui en ont besoin.

**Les applications existantes ?** Branchement par connecteurs, en lecture au départ, sans ressaisie.

**Pourquoi « Kairos » ?** En grec, le bon moment.

## Sur les chiffres

**Que mesurent les 95,4 % et 55,3 % ?** Les déclarations de 152 tribunaux judiciaires à l’IGJ (enquête déclarative), pas ce que reçoivent les victimes. C’est précisément ce que Kairos permettrait de mesurer. Le pitch dit « à peine un tribunal sur deux », exact pour 55,3 %.

**Que signifient les 12 371 caducités ?** Parmi les 440 460 décisions de cours d’appel publiées sur Judilibre (janvier 2022 à septembre 2026), 12 371 appels sont déclarés caducs, souvent pour un délai manqué. C’est environ 2,8 %. Judilibre ne publie qu’une partie des décisions : ne pas le lire comme un total national. Il illustre « chaque décision crée des obligations pour quelqu’un », pas la démonstration. Contrôle manuel : 23 résultats justes sur 24, échantillon trop petit pour annoncer un taux. Voir [les points de vigilance](points-de-vigilance.md).

## Sur le droit

**« Nul n’est censé ignorer la loi » : une décision non notifiée est-elle opposable ?** La maxime vise la loi, pas les décisions. Tant qu’une décision n’est pas notifiée, ses effets et les délais de recours ne courent pas, en principe : à confirmer par les juristes. L’idée du pitch est que l’information doit arriver pour que la décision protège.

**Kairos prend-il une décision automatisée ?** Non : aucune décision fondée sur un traitement automatisé (article 22 du RGPD, article 47 de la loi Informatique et libertés ; directive (UE) 2016/680 pour les données pénales). Il propose, le greffe décide.

**Kairos dit-il qu’un acte est nul ?** Jamais. Il signale un risque (mention absente, avis non retrouvé), montre les sources, et le magistrat apprécie. Même formulation pour les rapprochements : jamais « même auteur ».

**Sur quel texte informer chaque destinataire ?** Les règles par type de décision sont à écrire avec des juristes. Le prototype n’en montre que quelques-unes à titre d’exemple. Aucun fondement n’est affirmé tant qu’il n’est pas validé. Piste à vérifier : une proposition de loi adoptée par l’Assemblée nationale le 12 mai 2026 créerait un article 10-2-1 du CPP (information de la victime un mois avant une libération), statut à vérifier.

## Sur la sécurité et l’hébergement

**Les données sensibles ?** Accès selon les habilitations, adresses protégées masquées, journal d’audit, pas de copie des dossiers. Détail dans [sécurité et données](securite-et-donnees.md).

**Et la victime ?** Pas d’accès direct par défaut ; l’information passe par son avocate ou un canal qu’elle choisit ; notifications neutres.

**L’hébergement ?** Application web dans un cloud souverain, interne à l’État ; exigences de souveraineté à cadrer avec le ministère (qualification SecNumCloud visée).

## Sur la suite

**Combien ça coûte ?** C’est l’objet du pilote : six mois dans un tribunal, trois mois pour mesurer la situation actuelle, trois mois pour mesurer l’effet de Kairos. Aucun chiffrage n’existe.

**Pourquoi commencer par les violences conjugales ?** C’est là que l’enjeu est le plus grave. Le mécanisme ne dépend pas du cas : il vaut pour toute décision qui doit parvenir à quelqu’un.

## Questions sans réponse arrêtée

- **Qualification au regard du règlement européen sur l’IA** : comment l’équipe se maintient dans la préparation administrative. À instruire.
- **Responsabilité si l’outil rate une alerte.** À instruire.
- **Branchement sur Cassiopée et les autres logiciels**, qui n’ont pas forcément d’API.
- **Adoption par les greffes** : ce que cela leur enlève comme travail, concrètement. Mesure prévue par le pilote.
- **Habilitations réelles** pour accéder aux fichiers de la police ou de la justice : on ne peut pas affirmer l’accès, seulement parler de connecteurs simulés.
