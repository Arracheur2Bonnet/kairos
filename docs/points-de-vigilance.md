# Points de vigilance

Ce qui n’est pas vérifié, ce qui diffère d’un livrable à l’autre, et ce qu’il reste à décider. Rien de ce qui suit n’est caché dans le dépôt : c’est la liste de ce qu’un lecteur attentif (un juriste, un membre du jury) pourrait relever. Dernière revue : 17 octobre 2026.

## 1. Sources à vérifier

**Le sens du 55,3 % (le plus important).** Le texte collé du rapport de l’IGJ dit : « seuls 55,3 % des TJ ont répondu *ne pas informer* la victime en cas d’infirmation par la CA de l’OP ». Lu à la lettre, 55,3 % des tribunaux n’informent pas. Dans la série de cinq taux décroissants introduite par « seuls », la lecture la plus probable est que 55,3 % informent, et c’est celle du dossier, du pitch, des diapositives et du README. Le prototype disait l’inverse ; il a été aligné le 17 octobre. Les archives et la vidéo de démonstration affichent encore « déclarent ne pas informer ». **À faire : ouvrir le rapport, page de la note 119, et trancher.** Si le sens est littéral, il faut corriger le pitch (« un tribunal sur deux ne prévient pas », ce qui est plus grave), le dossier, les diapositives et le README. Le site justice.gouv.fr était en maintenance les 15, 16 et 17 octobre : le PDF n’a pu être ouvert.

**Les pages du rapport.** Le dossier cite 95,4 % p. 52 et 55,3 % p. 45 ; le pitch précédent disait l’inverse (« p. 45 et 52 », dans l’ordre). Les deux chiffres et les notes 118 et 119 sont dans le même paragraphe, donc probablement à la même page ou sur deux pages voisines : une seule vérification règle les deux questions. Les diapositives disent « selon le dossier, à vérifier ».

**Le lien et le numéro du rapport.** Le lien collé par l’équipe contenait « igi » ; le fichier s’appelle `rapport_mission_igj_vif.pdf`. Rapport définitif n° 073-25, décembre 2025. Ne pas confondre avec le rapport d’étape n° 065-25 (novembre 2025), fichier `rapport_etape_mission_igj_vif.pdf`.

**152 tribunaux et caractère déclaratif.** Non vérifiés à la source (même raison). Le dossier et les diapositives disent « déclaratif » : à conserver, c’est ce qui protège de la première question d’un juriste.

**Judilibre.** Judilibre ne publie qu’une partie des décisions (pour les cours d’appel, selon nos recherches, les chambres civiles, commerciales et sociales depuis avril 2022 ; le pénal n’est pas confirmé). Donc : dire « parmi les 440 460 décisions publiées ». Vérifier que « janvier 2022 » est la date des décisions et non de leur publication. 12 371 caducités sur 440 460, c’est 2,8 %. La part due à un délai manqué n’est pas établie. Le contrôle manuel de 23 résultats justes sur 24 est un échantillon trop petit pour annoncer un taux (intervalle à 95 % d’environ 80 à 99 %) : le présenter comme un contrôle ponctuel, ou l’élargir à une centaine. Ce chiffre porte sur les délais en appel civil, pas sur l’information des victimes. Une piste : compter, dans le même corpus, les arrêts qui infirment une ordonnance de protection donnerait le volume réel du cas de la démonstration.

**Textes juridiques.** Les fondements par type de décision et par destinataire ne sont pas écrits (seul l’article 515-11 du code civil est ressorti pour les mesures de l’ordonnance de protection). La proposition de loi créant l’article 10-2-1 du CPP (adoptée par l’Assemblée nationale le 12 mai 2026) : statut à vérifier. Les règles du FIJAIS (déclaration d’adresse, délais, sanctions) viennent d’un blog d’avocat : vérifier l’article 706-53-5 du CPP avant tout usage. La qualification au regard du règlement européen sur l’IA (annexe III, domaine de la justice) est à instruire.

## 2. Ce que disent les livrables, et qui diffère

| Sujet | Écart | Conséquence |
|---|---|---|
| Cas du pitch et du prototype | Le pitch montre la cour d’appel qui annule l’interdiction de contact ; le prototype montre la libération de M. R. reçue de l’administration pénitentiaire ; le dossier écrit montre une demande de mise en liberté | Dire « une décision arrive, Kairos prépare l’avis » pendant la démonstration ; refonte du prototype non faite |
| Suivi « envoyé, distribué, consulté » | Absent du prototype, montré en diapositive 10 | Le dire |
| Vidéo de 41 secondes | Montre le déménagement, la ligne DGFiP et l’onglet Vigilance, que les consignes disaient de ne pas ouvrir ; affiche encore l’ancien libellé du 55,3 % ; ne montre ni l’analyse ni la validation | Refaire la vidéo sur le parcours recommandé si elle est diffusée (voir [demo.md](demo.md)) |
| PowerPoint | Les apparitions au clic de la version HTML ne sont pas reproduites ; l’image d’attente de la vidéo est une capture du prototype ; polices Arial | À ajuster dans PowerPoint si besoin |
| Dossier PDF | « Un homme condamné pour violences conjugales demande sa mise en liberté » : une demande de mise en liberté concerne en principe un détenu provisoire ou un condamné dont l’appel n’est pas jugé ; un condamné définitif demande plutôt un aménagement de peine ou une libération conditionnelle au juge de l’application des peines. Un juriste le relèvera. Formulations possibles : « en détention provisoire, il demande sa mise en liberté » ou « il demande une libération conditionnelle » | À décider |
| Dossier PDF | « Kairos … il … Elle ne remplace aucun logiciel » (le genre change au milieu de la phrase) ; « arrêtés » dans le texte, « déclarés caducs » dans les sources ; titre du fichier PDF « r.html » avant correction | Maladresses de forme ; la copie texte les conserve |
| Notes de la diapositive 9 | Contiennent des consignes de manipulation (« À NE PAS OUVRIR… », « ATTENTION… ») | Internes, à ne pas lire à voix haute |
| Contraintes du hackathon | Citées d’après une note collée, confirmées par l’équipe le 16 octobre 2026 | Réglé |

## 3. Choix de fond à connaître

- **Pas de note, pas de score, pas de qualification.** Kairos ne dit jamais « nul » ni « même auteur ». L’exercice a été fait pour deux pistes écartées : un « scoring » des audiences (remplacé par des alertes) et une « mise en cause commune » entre affaires (mot réservé à la procédure pénale, voir [les pistes](pistes-explorees.md)).
- **Pas de croisement avec des fichiers officiels dans le pitch** (impôts, état civil, FIJAIS, fichier des personnes recherchées) : base légale non établie. Ils restent dans le prototype et dans les archives.
- **Rien d’officiel dans le visuel** : pas de Marianne, de bloc « République française » ni de police de l’État ; le système de design de l’État est réservé aux sites publics. Le prototype a un aspect de service public (palette standard, Arial, boutons carrés), un badge « PROTOTYPE » et des données fictives. La palette vient d’une page publique de l’ANTS téléchargée, non republiée ici.
- **Le jury est composé de juristes** : le moins de technique possible, une seule diapositive technique.

## 4. Confidentialité et sécurité du dépôt

- Toutes les données sont fictives (tribunal de Valmont, Corbelle, noms inventés, prénoms français).
- Aucun nom de personne de l’équipe, aucun courriel, aucun chemin de poste de travail dans les fichiers suivis. L’identité de commit est l’adresse « noreply » de GitHub.
- Les métadonnées du PowerPoint (auteur « Steve Canny », date de 2013, issues du modèle de la bibliothèque qui l’a généré) ont été remplacées.
- Le dépôt est **privé**. Avant de le publier : relire ce fichier, vérifier la mention de l’équipe, choisir une licence. Le dépôt n’en a aucune : tous droits réservés.
- Les contenus de tiers (page de l’ANTS, guides de conception fournis pendant le travail) ne sont pas republiés.
- Un lien d’image temporaire d’un service de stockage figurait dans des textes collés : retiré.
- Recommandé côté GitHub : authentification à deux facteurs, et le réglage « Block command line pushes that expose my email ».

## 5. À décider

1. Le sens du 55,3 % (point 1).
2. La phrase « demande sa mise en liberté » dans le dossier.
3. Refaire ou non la vidéo, et le prototype sur le scénario du pitch.
4. La licence, et le passage du dépôt en public.
