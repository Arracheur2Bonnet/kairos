# La démonstration

Trois choses existent : le prototype cliquable, la vidéo de 41 secondes enregistrée par l’équipe, et le script de démonstration écrit pour la présentation. Ils ne racontent pas exactement la même histoire, ce qui est dit plus bas.

## Le prototype

[demo/kairos.html](../demo/kairos.html) est un fichier unique, sans installation ni connexion : on l’ouvre dans un navigateur (Chrome ou Edge) après avoir cloné le dépôt. Il n’envoie ni ne mémorise aucune donnée. Toutes les données sont fictives : le tribunal de Valmont, la greffière Claire L., M. Julien R. (l’auteur), Mme M. (la victime), Me Anne V., Me Paul D., M. Laurent T. et Mme Sophie B. (l’exemple du PV de garde à vue). Aucun logiciel réel n’est branché ; les noms Cassiopée, GENESIS, APPI, WinCI TGI, WinEURS, RPVA servent d’exemples de sources.

Quatre onglets, accessibles aussi par l’adresse : `#pilotage`, `#affaire`, `#actions`, `#vigilance`. Le bouton « Réinitialiser la démo », en bas de page, remet tout à zéro.

| Onglet | Ce qu’on y voit |
|---|---|
| Pilotage | La date du jour, « Le point de Kairos » (un résumé en langage clair, avec le nombre de contrôles faits depuis le matin), les alertes classées en « à traiter », « à vérifier » et « pour information », les audiences à venir (cinq cartes) avec seulement les affaires qui posent problème |
| Affaire R. / M. | Le schéma des quatre procédures liées à une même personne (pénal, ordonnance de protection, assistance éducative, divorce) ; l’événement entrant (la libération de M. R. le 29 octobre, reçue de l’administration pénitentiaire) ; le bouton « Analyser l’impact » qui déroule cinq étapes (l’IA lit l’événement, retrouve les dossiers liés, le moteur de règles encadre, l’IA prépare les actions, « ce que Kairos n’a pas fait ») ; la chronologie de l’année ; le bloc « Protection de Mme M. » ; le bloc « Informer la victime : où le risque se situe » (les cinq chiffres de l’IGJ) ; les données de l’affaire avec leur source et leur niveau de fiabilité |
| Actions | Six actions créées par l’analyse, chacune avec un responsable, une échéance et une source ; l’avis à la victime rédigé par l’IA, qu’on ne peut valider qu’après avoir coché trois vérifications ; le journal de traçabilité |
| Vigilance | « Analyser un acte » (un PV d’exemple de placement en garde à vue : l’IA surligne personnes, heures et actes, passe sept contrôles et constate qu’aucun avis au procureur n’y figure) ; le fil des contrôles ; les alertes détaillées avec leur cycle de vie (« Je prends en charge », escalade, compte à rebours) |

Il y a quatorze alertes (V-01 à V-12, V-14 et V-15). Cinq règles juridiques d’exemple sont affichées (R-VIF-01 à R-EXE-05), par exemple « libération d’une personne condamnée pour violences conjugales : vérifier si la victime a demandé à être informée, préparer l’avis, le soumettre à validation ». Un assistant (« Demander à Kairos ») répond à quelques questions prédéfinies à partir des données fictives : il ne fait tourner aucun modèle.

### Ce que le prototype ne montre pas

- Il simule une libération annoncée par la prison, pas l’annulation en appel du pitch.
- Il n’a pas le suivi « envoyé, distribué, consulté » ni l’alerte à la veille : ils sont montrés dans la présentation, diapositive 10.
- Après la validation de l’avis, il dit « transmis au circuit d’envoi » et n’envoie rien.
- Il ne montre ni le commissariat ni l’avocat comme destinataires de la même décision.
- Il contient des modules explorés en route qui ne font pas partie du pitch : l’assistant de questions, le déménagement de la victime (avec une mention du FIJAIS), l’alerte « avis d’imposition non conforme aux données de la DGFiP », l’inscription au fichier des personnes recherchées, la confirmation de l’état civil. La base légale de ces croisements n’est pas établie, voir [les pistes explorées](pistes-explorees.md).

## La vidéo

[demo/video-demo.mp4](../demo/video-demo.mp4), 41 secondes, sans son, enregistrée par l’équipe sur le prototype. Voici ce qu’elle montre, avec des repères approximatifs :

| Vers | Écran |
|---|---|
| 0:00 | Pilotage : « Jeudi 15 octobre », « Le point de Kairos à 10:04 », les alertes (dont la libération de M. R. le 29 octobre, une permission de sortir sans avis à la victime, une adresse protégée en clair dans un dossier de divorce) |
| 0:03 | La liste défile : alertes « à vérifier », dont une ligne « Avis d’imposition non conforme aux données de la DGFiP » |
| 0:05 | Audiences à venir : les cartes du 20 octobre au 5 novembre, avec leurs affaires à problème |
| 0:09 | Affaire R. / M. : les quatre procédures autour de la personne, l’événement entrant (le bouton « Analyser l’impact » n’est pas cliqué) |
| 0:14 | La chronologie de l’année, un événement sélectionné avec sa source |
| 0:25 | « Protection de Mme M. » (déménagement, carte avec communes et distances, mention du FIJAIS), puis « Informer la victime : où le risque se situe », avec les cinq barres de l’IGJ ; la dernière dit encore « 55,3 % des tribunaux déclarent ne pas informer » |
| 0:29 | Les données de l’affaire, avec leur source et leur fiabilité |
| 0:31 | Onglet Vigilance : « Analyser un acte », le PV d’exemple, les contrôles, « aucune mention d’un avis au procureur de la République » |
| 0:40 | La fiche de l’alerte « Garde à vue de M. Laurent T. : aucun avis au procureur retrouvé », avec les recherches faites et la conséquence possible (article 63 du code de procédure pénale) |

La vidéo ne montre donc ni l’analyse d’impact, ni la validation de l’avis, ni le suivi. Elle finit sur le contrôle d’un PV, c’est-à-dire sur la fonction « fiabiliser les données ».

**Écarts avec ce qui était prévu :** les consignes données pour la démonstration disaient de ne pas ouvrir l’onglet Vigilance, le déménagement ni la ligne de la DGFiP, car ils sortent du pitch. La vidéo les montre brièvement. Elle affiche aussi l’ancienne lecture du 55,3 % (« déclarent ne pas informer »), que le prototype a depuis été corrigé pour ne plus afficher. Si la vidéo est remontée en public, mieux vaut la refaire sur le parcours ci-dessous.

## Le parcours recommandé

Environ 45 secondes, huit clics, souris lente et pause d’une seconde après chaque clic.

| Temps | Écran | Action | À dire |
|---|---|---|---|
| 0:00 | Pilotage | Laisser l’écran 5 secondes | « L’écran de la greffière. Ce matin, Kairos a déjà repéré des irrégularités. Et voici la libération de M. R. : la date vient d’arriver. » |
| 0:10 | Pilotage | Clic 1 : la première alerte rouge, « Libération prévisionnelle de M. Julien R. » | |
| 0:12 | Affaire R. / M. | Clic 2 : « Analyser l’impact », attendre les cinq étapes (environ 4 secondes) | « Quatre procédures, trois logiciels. Kairos retrouve les dossiers, applique les règles, prépare les actions. » |
| 0:24 | Affaire R. / M. | Clic 3 : « Voir les 6 actions » | |
| 0:27 | Actions | L’avis à la victime est déjà ouvert. Clics 4 à 6 : cocher les trois cases | « L’avis à la victime, rédigé en mots simples. Trois vérifications. » |
| 0:38 | Actions | Clic 7 : « Valider l’avis » | « Le greffier valide d’un clic. Tout est tracé. » |
| 0:45 | Actions | Rester 3 secondes sur le message de confirmation | |

Pendant la démonstration, dire « une décision arrive, Kairos prépare l’avis » plutôt que « demande de mise en liberté » : le prototype part d’une libération, pas d’une décision d’appel.

**À ne pas ouvrir :** l’action n° 6 (elle cite la DGFiP), l’onglet Vigilance, « Demander à Kairos », le déménagement de Mme M.

### Pour enregistrer la vidéo

1. Ouvrir `demo/kairos.html` dans Chrome ou Edge en plein écran (F11), zoom à 125 %, autres onglets, notifications et favoris fermés. Recharger la page juste avant.
2. Enregistrer sans son (Windows + Maj + R avec l’outil Capture d’écran, ou Windows + Alt + R avec la barre de jeu) : le commentaire se fait en direct, ce qui évite de recaler la voix.
3. S’entraîner deux fois, puis enregistrer. Si un clic rate, recommencer : la vidéo dure moins d’une minute.
4. Déposer le fichier dans `demo/` à côté de `kairos.html`.

## Variantes du commentaire

**Environ 45 secondes (diapositive 9 du PowerPoint).** Reprend le tableau ci-dessus.

**Environ 70 à 80 secondes (version plus complète).**

1. *L’écran du greffe, 20 s.* « Voici l’écran de la greffière, jeudi 15 octobre. Depuis ce matin, Kairos a lu les actes qui sont arrivés et il alerte. Regardez : une permission de sortie, le 12 septembre, sans aucun avis à la victime. Une adresse protégée écrite en clair dans un dossier de divorce. Ce sont des irrégularités que personne n’avait vues. Et en tête, ce qui nous intéresse : la date de libération de M. R. vient d’arriver de GENESIS, à 9 h 42. » Clic sur la première alerte.
2. *L’affaire, 25 s.* « Quatre procédures le concernent, dans trois logiciels différents. » Clic sur « Analyser l’impact ». « Kairos lit l’événement, retrouve les dossiers liés, applique les règles, prépare les actions. Et il précise ce qu’il n’a pas fait : aucun envoi, aucune mesure modifiée. » Clic sur « Voir les 6 actions ».
3. *La validation, 30 s.* « Six actions, chacune avec un responsable et une échéance. La première : l’avis à la victime. » L’ouvrir. « Kairos a rédigé le message, en mots simples. Il vérifie trois choses : la victime a demandé à être informée, l’envoi part chez son avocate et non à son adresse, et le projet est relu. » Cocher les trois cases, « Valider l’avis ». « Le greffier valide d’un clic. C’est tracé, horodaté, au journal. »
4. *Retour aux diapositives, 5 s.* « Et ensuite, comme pour un colis : envoyé, distribué, consulté. » La diapositive 10 montre ce suivi.

## Ce qu’il faudrait pour que la démonstration colle au pitch

Refaire le prototype sur le scénario du pitch : décision de la cour d’appel qui annule l’interdiction de contact, trois destinataires (victime, avocat, police) avec leur texte de référence, envoi après validation, puis suivi envoyé, distribué, consulté et alerte au greffe. Une version de ce type, avec des accusés qui reviennent et une relance à 24 heures, existe dans [les archives](../archives/chronos-circulation/prototype.html) (version « circulation », abandonnée à l’époque pour d’autres raisons) : on peut s’en inspirer. Cette refonte n’a pas été faite.
