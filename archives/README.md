# Archives

Tout ce qui a précédé la version finale de Kairos. Rien n’a été supprimé : le dépôt est la seule source du projet, et les anciennes versions gardent des idées, des formulations et des écrans qui ont servi à en construire d’autres. Ce sont des pages HTML autonomes : on les ouvre dans un navigateur, sans connexion.

## À lire avant d’ouvrir

- **Les archives gardent leur formulation d’époque.** Elles s’appellent « Vigie » puis « Chronos », elles contiennent des pistes abandonnées (rapprochement d’affaires, assistant de questions, croisements avec les impôts, le FIJAIS ou le fichier des personnes recherchées), et la plupart affichent encore « 55,3 % des tribunaux déclarent ne pas informer ». La lecture retenue depuis est « informent », voir [les points de vigilance](../docs/points-de-vigilance.md). Ne pas citer une archive comme la position actuelle.
- **Les prénoms ont été francisés dans toutes les archives** (M. Karim T. est devenu M. Laurent T., Mme Inès B. est devenue Mme Sophie B.), comme dans la version finale.
- **Aucune archive ne contacte l’extérieur.** La première version du prototype chargeait des polices depuis un service tiers : ces lignes ont été retirées, la page utilise les polices du système et son aspect diffère légèrement de l’original.
- **Les boutons « Ouvrir le prototype » des anciennes présentations** ouvrent la dernière version Chronos du prototype ([prototype-v13](versions-intermediaires/prototypes/prototype-v13.html)) ou le prototype actuel ([demo/kairos.html](../demo/kairos.html)), selon l’époque.
- **Toutes les données sont fictives.**

## Les quatre étapes

1. **Vigie procédurale** (15 octobre, de 11 h 52 à 14 h 26). Une « tour de contrôle » qui vérifie l’état des procédures et relie les dossiers d’une même affaire. Deux moteurs : un scanner de vigilance (le PV de garde à vue dont l’avis au procureur manque) et un moteur de liens entre affaires, retiré à 14 h 08. Passage à un thème blanc, sans note, avec des alertes.
2. **Chronos, tour de contrôle** (de 14 h 26 à 16 h 55). Renommage, habillage de service public sans reprendre les marques de l’État, IA au premier plan, alertes qui ne se perdent jamais, assistant de questions, victime qui déménage, données certifiées, chiffres de l’IGJ, problématique de l’équipe, puis un bloc de sécurité de six diapositives et une présentation pensée pour un jury de juristes.
3. **Chronos, agent de circulation** (de 15 h 06 à 15 h 43). Une reconstruction autour de la circulation d’une décision (destinataires, validation, accusés de réception, relance à 24 heures, mesure), faite à partir du pitch v3. L’équipe a jugé qu’elle s’éloignait trop de ce qu’elle voulait : retour à l’étape 2, cette version est gardée à part.
4. **Kairos** (à partir de 16 h 54). Nouveau dossier rédigé, « le suivi de colis de la justice », puis deux versions de la présentation avant la version finale, qui est à la racine du dépôt.

Le récit complet, avec les décisions et leurs raisons, est dans [docs/historique.md](../docs/historique.md).

## Index

### Chronos, tour de contrôle (étape 2)

| Fichier | Contenu |
|---|---|
| [chronos-presentation-tour-de-controle.html](chronos-presentation-tour-de-controle.html) | Présentation de 24 diapositives : 11 de pitch, puis la sécurité, les standards, l’interservices, la gestion des alertes, l’assistant, la victime qui déménage, les données certifiées et les briques Microsoft. C’est la version complète de cette époque, avec toutes les annexes. |
| [versions-intermediaires/prototypes/prototype-v13.html](versions-intermediaires/prototypes/prototype-v13.html) | Dernier état du prototype de cette époque (sauvegarde de 15 h 20), avec les chiffres de l’IGJ, le déménagement et les données certifiées. |

### Chronos, agent de circulation (étape 3)

| Fichier | Contenu |
|---|---|
| [chronos-circulation/pitch.md](chronos-circulation/pitch.md) | Le pitch de l’équipe (v3) repris en version 4, avec la démonstration clic par clic et une liste de vérifications. 501 mots, environ 3 min 35 s sans la démonstration. |
| [chronos-circulation/presentation.html](chronos-circulation/presentation.html) | 11 diapositives chronométrées sur ce pitch et 5 d’annexe (sous le capot, cadre juridique, pour aller plus loin, méthode et sources, captures de secours). |
| [chronos-circulation/prototype.html](chronos-circulation/prototype.html) | Prototype reconstruit : décisions, suivi de la circulation (agrégé par type de décision, jamais par agent), alertes, extensions. Une démonstration en deux clics, de l’arrêt qui infirme l’ordonnance de protection jusqu’à la relance à 24 heures. |

### Kairos, premières présentations (étape 4)

| Fichier | Contenu |
|---|---|
| [kairos-pitch-v1/pitch-v1-20-diapos-avec-annexes.html](kairos-pitch-v1/pitch-v1-20-diapos-avec-annexes.html) | Première présentation sur le dossier Kairos : 12 diapositives de pitch (ouverture sur une paire de chaussettes, démonstration sur une demande de mise en liberté), une diapositive de sécurité et 7 annexes (sources et méthode, questions attendues, détail de la sécurité). |
| [kairos-pitch-v1/pitch-v1-12-diapos.html](kairos-pitch-v1/pitch-v1-12-diapos.html) | La même, coupée après la diapositive de demande : sans sécurité ni annexes. |
| [kairos-pitch-v1/pitch-v1-13-diapos.html](kairos-pitch-v1/pitch-v1-13-diapos.html) | Avec la diapositive « Le squelette de Kairos » avant la démonstration (sources, ce que fait l’IA, ce que fait la plateforme). |
| [kairos-pitch-v1/pitch-v1-13-diapos-derniere-version.html](kairos-pitch-v1/pitch-v1-13-diapos-derniere-version.html) | Dernier état avant la mise à jour du dossier : « risques de nullité » et « mentions obligatoires » dans l’analyse, « elle alerte sur les irrégularités » dans la plateforme, démonstration raccourcie à 45 secondes. Le texte de ce pitch est reconstitué dans [textes-d-origine](textes-d-origine/06-pitch-kairos-v1-reconstitue.md). |
| [kairos-pitch-v2/pitch-v2-14-diapos.html](kairos-pitch-v2/pitch-v2-14-diapos.html) | Présentation reconstruite sur le nouveau texte du dossier (ouverture sur « Qui, ici, a reçu un colis cette semaine ? », cour d’appel qui annule l’interdiction, trois fonctions, trois enjeux). 14 diapositives ; la dernière diapositive de demande a ensuite été retirée pour donner la version finale à 13. |

### Versions intermédiaires de la présentation

Ce sont des sauvegardes faites avant chaque série de modifications, du matin du 15 octobre à la fin de l’étape 2. L’heure est celle de la sauvegarde, c’est-à-dire l’état juste avant la modification suivante.

| Fichier | Heure | Diapositives | Ce qu’elle contient |
|---|---|---|---|
| [presentation-v01](versions-intermediaires/presentations/presentation-v01.html) | 14 h 09 | 12 | « Vigie » : le cas, deux moteurs, le PV de garde à vue, l’escroquerie, une donnée une source, des alertes, qui décide, sous le capot |
| [presentation-v02](versions-intermediaires/presentations/presentation-v02.html) | 14 h 25 | 11 | Sans l’escroquerie (rapprochement retiré) |
| [presentation-v03](versions-intermediaires/presentations/presentation-v03.html) | 14 h 29 | 11 | Renommée « Chronos » |
| [presentation-v04](versions-intermediaires/presentations/presentation-v04.html) | 14 h 56 | 12 | IA au premier plan : ce que fait l’IA, l’assistant, l’humain valide, problématique |
| [presentation-v05](versions-intermediaires/presentations/presentation-v05.html) et [v05b](versions-intermediaires/presentations/presentation-v05b.html) | 15 h 20 et 15 h 46 | 16 | Ajout du point faible (chiffres de l’IGJ), d’une alerte qui ne se perd jamais, de la victime qui déménage et des données certifiées |
| [presentation-v06](versions-intermediaires/presentations/presentation-v06.html) | 15 h 47 | 16 | Problématique de l’équipe en diapositive 3 ; 10 diapositives de pitch et 6 annexes |
| [presentation-v07](versions-intermediaires/presentations/presentation-v07.html) | 16 h 07 | 16 | Polices agrandies au maximum |
| [presentation-v08](versions-intermediaires/presentations/presentation-v08.html) | 16 h 27 | 19 | Trois diapositives de sécurité (accès, partout et standards, interservices) |
| [presentation-v09](versions-intermediaires/presentations/presentation-v09.html) | 16 h 33 | 24 | Six diapositives de sécurité (chaque risque, puis sa réponse), puis standards et interservices |

Pour les prototypes, les sauvegardes sont dans [versions-intermediaires/prototypes](versions-intermediaires/prototypes/) : prototype-v01 à v13, sans v12 (cette sauvegarde n’a jamais été faite). La matrice ci-dessous dit ce que contient chacune.

### Matrice des fonctionnalités du prototype, version par version

« oui » signifie que la fonction apparaît dans le fichier. Les trois dernières lignes sont la dernière version Chronos (v13), la version « circulation » et le prototype actuel.

| Version | Heure | Titre | Onglets | Scanner de PV | Rapprochements | Assistant | Déménagement | Cycle des alertes | Données certifiées | Bloc IGJ | Fichiers FIJAIS, FPR, DGFiP |
|---|---|---|---|---|---|---|---|---|---|---|---|
| [v01](versions-intermediaires/prototypes/prototype-v01.html) | 12:23 | Vigie procédurale | Pilotage, Affaire R. / M., Actions, Vigilance, Architecture |  |  |  |  |  |  |  |  |
| [v02](versions-intermediaires/prototypes/prototype-v02.html) | 12:35 | Vigie procédurale | Pilotage, Affaire R. / M., Rapprochements, Actions, Vigilance, Architecture |  | oui |  |  |  |  |  |  |
| [v03](versions-intermediaires/prototypes/prototype-v03.html) | 12:43 | Vigie procédurale | Pilotage, Affaire R. / M., Rapprochements, Actions, Vigilance, Architecture | oui | oui | oui |  |  |  |  |  |
| [v04](versions-intermediaires/prototypes/prototype-v04.html) | 13:52 | Vigie procédurale | Pilotage, Affaire R. / M., Rapprochements, Actions, Vigilance, Architecture | oui | oui | oui |  |  |  |  |  |
| [v05](versions-intermediaires/prototypes/prototype-v05.html) | 14:09 | Vigie procédurale | Pilotage, Affaire R. / M., Rapprochements, Actions, Vigilance | oui | oui | oui |  |  |  |  |  |
| [v06](versions-intermediaires/prototypes/prototype-v06.html) | 14:16 | Vigie procédurale | Pilotage, Affaire R. / M., Actions, Vigilance | oui |  | oui |  |  |  |  |  |
| [v07](versions-intermediaires/prototypes/prototype-v07.html) | 14:21 | Vigie procédurale | Pilotage, Affaire R. / M., Actions, Vigilance | oui |  | oui |  |  |  |  |  |
| [v08](versions-intermediaires/prototypes/prototype-v08.html) | 14:25 | Vigie procédurale | Pilotage, Affaire R. / M., Actions, Vigilance | oui |  | oui |  |  |  |  |  |
| [v09](versions-intermediaires/prototypes/prototype-v09.html) | 14:29 | Chronos | Pilotage, Affaire R. / M., Actions, Vigilance | oui |  | oui |  |  |  |  |  |
| [v10](versions-intermediaires/prototypes/prototype-v10.html) | 14:36 | Chronos | Pilotage, Affaire R. / M., Actions, Vigilance | oui |  | oui |  |  |  |  |  |
| [v11](versions-intermediaires/prototypes/prototype-v11.html) | 14:54 | Chronos | Pilotage, Affaire R. / M., Actions, Vigilance | oui |  | oui |  |  |  |  |  |
| [v13](versions-intermediaires/prototypes/prototype-v13.html) | 15:20 | Chronos | Pilotage, Affaire R. / M., Actions, Vigilance | oui |  | oui | oui | oui | oui | oui | oui |
| [circulation](chronos-circulation/prototype.html) |  | Chronos | Décisions, Suivi, Alertes, Affaire R. / M., Extensions | oui |  | oui | oui | oui |  |  |  |
| [Kairos (actuel)](../demo/kairos.html) |  | Kairos | Pilotage, Affaire R. / M., Actions, Vigilance | oui |  | oui | oui | oui | oui | oui | oui |

À lire ainsi : le scanner de PV, présent dès v03, est resté jusqu’au prototype actuel (la vidéo de démonstration finit dessus). Le rapprochement d’affaires n’existe que de v02 à v05. L’assistant de questions, le déménagement, les données certifiées et les croisements avec des fichiers officiels sont dans le prototype actuel, mais **ne font pas partie du pitch** : voir [les pistes explorées](../docs/pistes-explorees.md).

### Textes d’origine

Les textes sur lesquels le projet s’est construit sont dans [textes-d-origine](textes-d-origine/00-LISEZMOI.md) : idée de départ, deuxième idée, données de l’IGJ, pitch Chronos v3, note de conception sur la sécurité, pitch Kairos v1 reconstitué.
