# Historique

Comment le projet est passé d’une « tour de contrôle » à Kairos en deux jours, avec les décisions de l’équipe et leurs raisons. Heures de Paris. Le matériel de chaque étape est dans [les archives](../archives/README.md).

## Chronologie

### Jeudi 15 octobre 2026

| Heure | Ce qui s’est passé |
|---|---|
| 11 h 49 | L’équipe expose son idée : une « tour de contrôle procédurale intelligente » ([texte](../archives/textes-d-origine/01-idee-de-depart.md)). Premier prototype cliquable, « Vigie procédurale », sur un événement qui traverse quatre procédures : la libération de M. R. le 29 octobre, reliée au pénal, à l’ordonnance de protection, au divorce et à l’assistance éducative |
| 12 h 09 | Deuxième idée : contrôle continu et rapprochement d’affaires ([texte](../archives/textes-d-origine/02-deuxieme-idee-rapprochement.md)). Le « scanner » est présenté comme de la vigilance, jamais comme un scanner de nullités |
| 12 h 30 | Consigne : pas de scoring, des alertes ; thème blanc. Exemple du PV de garde à vue sans avis au procureur. Puis deux fonctions de plus : demandes de libération et sorties sur la frise avec les avis à la victime, envoi des convocations aux audiences |
| 13 h 52 | Prototype allégé, présentation HTML interactive de 12 diapositives, chronométrée, avec notes |
| 14 h 06 | L’équipe demande une problématique ; trois formulations proposées |
| 14 h 08 | Le rapprochement d’affaires est retiré du prototype et des diapositives |
| 14 h 16 | Application du guide de design fourni par l’équipe |
| 14 h 22 | Habillage « service public » sans copier le site du ministère : le système de design de l’État est réservé à ses sites, rien de la Marianne ni du bloc « République française » |
| 14 h 26 | Le projet devient **Chronos** |
| 14 h 29 | Reprise de la palette d’une page publique de l’ANTS (couleurs seulement) |
| 14 h 42 | L’IA est mise au premier plan : « le point de Chronos », assistant de questions, explications |
| 14 h 47 | Pistes demandées par l’équipe : le déménagement de la victime et les fichiers, l’alerte comme produit, les impôts pour l’authenticité des informations ([pistes](pistes-explorees.md)). Intégrées au prototype à 14 h 57 |
| 14 h 59 | Intégration des chiffres de l’IGJ collés par l’équipe ([texte](../archives/textes-d-origine/03-donnees-igj.md)), avec un doute sur le sens du 55,3 % |
| 15 h 01 | L’équipe colle son pitch « verdict final » (v3), en gardant sa problématique ([texte](../archives/textes-d-origine/04-pitch-chronos-v3.md)). Analyse des écarts avec le prototype, plan validé |
| 15 h 37 | Reconstruction autour de la circulation d’une décision (version « circulation ») |
| 15 h 43 | **Retour arrière demandé par l’équipe** : la reconstruction va trop loin. Elle est mise de côté |
| 15 h 46 | La problématique de l’équipe est en diapositive 3 ; 10 diapositives de pitch pour 5 minutes |
| 16 h 04 | Polices agrandies au maximum, sans tout casser |
| 16 h 07 à 16 h 29 | Bloc de sécurité à partir de la note collée ([texte](../archives/textes-d-origine/05-conception-securite-interservices.md)) : d’abord une diapositive, puis trois, puis six (risque, puis réponse). Consigne : montrer qu’on est sécurisé, double authentification comprise |
| 16 h 37 | Refonte pour un jury de juristes : 11 diapositives courtes, une seule diapositive technique (la sécurité), l’effet de surprise, le moins d’informations inutiles ; le reste en annexe |
| 16 h 38 | Prénoms français partout (Karim devient Laurent, Inès devient Sophie) |
| 16 h 54 | **Pivot : Kairos.** L’équipe fournit un dossier rédigé, « le suivi de colis de la justice » ([Kairos-dossier-redige.pdf](../Kairos-dossier-redige.pdf)). Décisions : garder la problématique de l’équipe (lourdeur procédurale), une démonstration au milieu, adapter le site ensuite, appliquer les corrections juridiques proposées |
| 17 h 01 | Présentation Kairos de 13 diapositives et 7 annexes. Le site est renommé Kairos (17 h 09) |
| 17 h 08 à 17 h 25 | Retouches : diapositive 6 allégée (l’équipe voulait garder les blocs, pas le gros texte), diapositives de la démonstration et du « squelette » (sources, ce que fait l’IA, ce que fait la plateforme), « mentions obligatoires, risques de nullité », « elle alerte sur les irrégularités ». Le texte de ce pitch : [reconstitué](../archives/textes-d-origine/06-pitch-kairos-v1-reconstitue.md) |
| 17 h 14 | Les diapositives après la douzième (sécurité et annexes) sont supprimées : l’équipe préfère une seule diapositive de démonstration |
| 17 h 30 | Démonstration ramenée à 45 secondes, gestes pour l’enregistrer en vidéo |
| 17 h 35 | Nouvelle version du dossier : nouvelle ouverture (« Qui, ici, a reçu un colis cette semaine ? »), cour d’appel qui annule l’interdiction de contact, trois fonctions, trois enjeux. Présentation reconstruite sur ce texte (14 diapositives, sans annexes ni sécurité) |
| 17 h 44 | La diapositive « La demande » est retirée (13 diapositives) ; export PowerPoint avec la vidéo de l’équipe incorporée ([Kairos.pptx](../Kairos.pptx)) |
| 17 h 47 | Deux courts pitchs demandés : la diapositive 7 et la vidéo ([pitch](pitch.md)) |

L’équipe a ensuite remporté le hackathon.

### Vendredi 16 octobre 2026

| Heure | Ce qui s’est passé |
|---|---|
| 14 h 23 | Mise du projet sur GitHub, dans un dépôt privé ; la vidéo y est ajoutée |
| 14 h 33 | README : contexte du hackathon, constat, solution avec le « pourquoi », schémas. Consignes : pas de style « IA », concret, avec les informations de la présentation, du site et des échanges |
| 14 h 56 | « Coup de balai » : contrôle du fond, de la forme, de la confidentialité, de la sécurité et de la complétude du dépôt, qui doit devenir la seule source du projet. Consignes : ne nommer aucune récompense ; l’équipe reste anonyme (décrite seulement par ses profils, sans écoles) ; contraintes du hackathon confirmées. Ce travail est celui de ce dossier |

## Consignes de l’équipe

Ce que l’équipe a demandé, et qui est resté vrai tout du long.

- **Problématique** : « comment transformer la lourdeur procédurale en levier d’efficacité au service de l’état de droit ? » À garder, dans tous les supports.
- **Pas de scoring** : des alertes, pas de notes ni de classements. L’IA signale, le professionnel décide.
- **Thème blanc.** Interface sobre, sans majuscules décoratives ni séparateurs en points.
- **Jury de juristes** : le moins technique possible, effet de surprise, aucune information inutile, une seule diapositive technique.
- **Pitch de 5 minutes** : texte raccourci, polices de diapositives les plus grandes possible sans tout casser.
- **Prénoms français partout**, villes fictives (Valmont, Corbelle), aucune donnée réelle.
- **Pas de marques de l’État** : ni Marianne, ni « République française », ni code du système de design de l’État.
- **Dire ce qui est promis** : sécurité affirmée par des engagements précis, non par « sécurité totale ».
- **Ne rien modifier au-delà de ce qui est demandé** : l’équipe a corrigé deux fois des interprétations trop larges (la reconstruction « circulation », la diapositive 6).

## Principes de conception

- L’IA propose, un humain valide, la plateforme envoie et prouve.
- Une brique branchée sur l’existant, pas un logiciel de plus.
- Une information saisie une fois, tracée partout, avec sa source, son auteur et sa version.
- Rien n’est qualifié juridiquement par l’outil : jamais « nul », jamais « même auteur ».
- Les adresses d’une victime sont datées, sourcées, jamais devinées ; au moindre doute, on confirme avant d’envoyer.
- Les indicateurs sont agrégés par service ou par type de décision, jamais par agent.
- Les chiffres déclaratifs sont présentés comme tels.
