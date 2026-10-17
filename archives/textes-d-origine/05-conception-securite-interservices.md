# Conception : sécurité, accès et interservices

Texte du 15 octobre 2026, 16 h 07. Pour la sécurité et l’échange entre services, l’équipe a collé une note de conception rédigée avec un assistant d’écriture, en demandant de la remettre en question. Le projet y porte un autre nom, « Syndeo », qui n’a jamais été le nôtre : c’est un nom de travail de l’auteur de la note. L’équipe a répondu : « On garde Chronos et on met toutes les promesses. »

**Ce qu’on y trouve.** Un principe (relier les données sans les copier, les faire circuler sous contrôle, prouver qui a vu quoi), des règles de sécurisation, trois niveaux d’accès avec double authentification, un accès sur tous les appareils, un serveur d’échange entre services pour les réquisitions, de l’automatisation à l’intérieur d’un service, des standards ouverts, une démonstration à trois écrans et des risques à anticiper.

**C’est aussi la source des quatre contraintes du hackathon** citées dans le README : « validation humaine avant toute modification, journalisation des accès et modifications, protection des données des justiciables, usage de standards d’échange ouverts ». L’équipe les a confirmées le 16 octobre 2026.

**Ce que nous en avons fait.** Une cible de conception de la sécurité (six risques, six réponses, matrice des droits, double authentification par profil, traçabilité, preuves avant le pilote), présentée d’abord en diapositives, puis retirée du pitch final à la demande de l’équipe. Elle est reprise, avec les points que nous avons remis en question, dans [sécurité et données](../../docs/securite-et-donnees.md). Les réquisitions n’ont pas été retenues : elles relèvent de l’enquête, pas de la circulation d’une décision.

## Le message de l’équipe

> Niveau sécurité, il faudrait une diapositive sur ces sujets. Remets-les en question :

## La note collée, telle quelle

> La sécurité et l'interservices peuvent devenir **la colonne vertébrale technique de Syndeo**. Il faut les présenter comme une architecture cible, et seulement simuler une partie en démo. Je n'ai pas pu vérifier ici les systèmes ni les habilitations réels de la justice française. Ce qui suit est donc du raisonnement et des hypothèses, à valider avec votre avocat et vos juristes.
>
> ## Le principe directeur
>
> > **Syndeo ne copie pas les données : il les relie, les fait circuler sous contrôle et prouve qui a vu quoi.**
>
> Le track impose la validation humaine avant toute modification, la journalisation des accès et modifications, la protection des données des justiciables et l'usage de standards d'échange ouverts. Votre architecture de sécurité répond à ces garde-fous. [image jointe : lien d’origine retiré]
>
> ## Sécurisation des données
>
> - **Minimisation**: chaque acteur ne voit que ce qui est nécessaire à sa mission. Une adresse protégée s'affiche masquée sauf pour un profil expressément habilité.
> - **Pas de base centrale dupliquée**: Syndeo interroge les systèmes sources et conserve des références, des métadonnées et des liens, plutôt que de recopier les dossiers.
> - **Chiffrement**: en transit et au repos, avec des clés gérées dans un coffre dédié.
> - **Journalisation inviolable**: chaque consultation, import, validation et envoi est tracé (auteur, heure, motif, source). Ce journal sert aussi de preuve de conformité.
> - **Données fictives en démo**: c'est la seule position défendable pendant le hackathon.
>
> ## Accès sécurisé et multi-authentification
>
> Je distingue trois niveaux d'accès, chacun avec des exigences différentes.
>
> | Profil | Authentification suggérée | Périmètre |
> |---|---|---|
> | Magistrat, greffier, agent | Authentification forte (carte ou clé physique + code) | Dossiers de sa juridiction ou de son service |
> | Avocat | Authentification forte liée à son identité professionnelle | Dossiers de ses clients uniquement |
> | Victime ou justiciable | Double authentification simple (code temporaire, application), canal sécurisé | Messages validés et informations autorisées |
>
> Quelques règles à afficher dans votre pitch:
>
> - **Moindre privilège**: aucun profil n'a un accès « par défaut » à tout.
> - **Droits par rôle et par contexte**: l'accès dépend du métier, du dossier et du motif. Exemple: l'agent chargé des enfants ne voit pas les données pénales qui ne lui sont pas nécessaires.
> - **Réauthentification** avant toute action sensible (validation d'une notification, accès à une donnée protégée).
> - **Aucune donnée sensible dans les notifications externes**: pas de SMS ni d'e-mail détaillé, seulement « une information est disponible dans votre espace sécurisé ».
> - **Sessions courtes** et alerte en cas de connexion inhabituelle.
>
> ## Accès cross-platform
>
> L'idée est que le professionnel retrouve le même dossier et les mêmes alertes sur poste fixe, tablette et mobile, sans multiplier les copies locales.
>
> - **Application web responsive** plutôt que des applications séparées.
> - **Aucune donnée persistante sur l'appareil**: pas de téléchargement par défaut, pas de cache sensible.
> - **Notifications « neutres »** sur mobile, par exemple « 1 action en attente », sans contenu.
> - **Verrouillage et déconnexion automatiques**, avec possibilité de révoquer un appareil à distance.
> - **Même moteur de droits** quel que soit l'appareil.
>
> Cela se rapproche de la vision d'un accès « partout » sans créer de nouvelle surface de fuite.
>
> ## Serveur interservices de réquisitions
>
> C'est ici qu'est votre vraie valeur ajoutée. Une réquisition est une demande formelle adressée à un service ou à un tiers pour obtenir des informations utiles à une procédure. Je ne détaille pas ici le cadre légal exact: vos juristes devront le préciser.
>
> Aujourd'hui, la difficulté probable est la suivante (hypothèse à confirmer par votre retour de terrain):
>
> - les mêmes informations sont ressaisies dans chaque demande;
> - le suivi des délais et des réponses se fait à la main;
> - la réponse est parfois difficile à rattacher au bon dossier;
> - les échanges passent par des canaux hétérogènes.
>
> ### Le rôle de Syndeo
>
> Syndeo jouerait le rôle d'un **hub d'échange sécurisé entre services**, avec trois fonctions:
>
> 1. **Pré-remplir** la demande à partir des données déjà présentes et sourcées, sans ressaisie.
> 2. **Acheminer** la demande vers le bon destinataire par un canal sécurisé, avec accusé de réception.
> 3. **Suivre et rattacher** la réponse au dossier: statut, délai, relance, version.
>
> ### Chaîne proposée
>
> ```text
> Besoin d'information identifié (événement ou dossier)
>         ↓
> Projet de réquisition pré-rempli avec sources
>         ↓
> Contrôle de cohérence (identités, références, pièces)
>         ↓
> Validation par l'autorité habilitée
>         ↓
> Signature et envoi par canal sécurisé
>         ↓
> Accusé de réception et suivi du délai
>         ↓
> Réponse rattachée au dossier avec sa provenance
>         ↓
> Journalisation complète
> ```
>
> ## Automatisation intra-service
>
> À l'intérieur d'un même service, l'automatisation vise surtout les tâches répétitives qui n'impliquent aucune appréciation juridique.
>
> - Remplir automatiquement les champs d'identité et de référence.
> - Vérifier que les pièces jointes annoncées sont présentes.
> - Rappeler les échéances et relancer une réponse en attente.
> - Répartir les tâches selon des règles objectives (type de demande, charge, disponibilité).
> - Proposer des modèles de demande classés par type.
> - Montrer au responsable la charge par agent et les blocages.
>
> **Ce qui reste humain**: le choix de lancer la demande, sa signature, sa transmission et toute décision qui en découle. Il ne faut jamais présenter l'outil comme un système qui « envoie des réquisitions tout seul ».
>
> ## Standards et interopérabilité
>
> Le track demande des standards d'échange ouverts. Votre argumentaire peut s'appuyer sur: [image jointe : lien d’origine retiré]
>
> - des **API documentées** entre services, plutôt que des connexions sur mesure;
> - des **formats structurés** (JSON ou XML) pour les données échangées;
> - un **identifiant de dossier et d'événement commun**, qui garantit qu'une donnée est saisie une fois et tracée partout;
> - la **conservation de la source, de l'auteur et de la version** pour chaque donnée.
>
> ## Ce que je montrerais en démo
>
> Ne tentez pas de simuler tout le réseau judiciaire. Montrez trois choses:
>
> 1. **Un écran de connexion** avec double authentification simulée et profils différents (professionnel, victime).
> 2. **Une réquisition pré-remplie** à partir d'un événement, avec les sources visibles et un bouton de validation humaine.
> 3. **Le journal** qui affiche qui a consulté, validé et envoyé quoi, et quand.
>
> Phrase pour le jury:
>
> > « Syndeo ne centralise pas les données: il fait circuler l'information sous contrôle. Chaque accès est authentifié, chaque envoi est validé par un humain et chaque action est tracée. »
>
> ## Risques à anticiper
>
> - **Habilitations réelles**: vous ne pouvez pas affirmer que l'outil accède à des fichiers de police ou de justice. Parlez de « connecteurs simulés ».
> - **Surpromesse sécuritaire**: évitez de prétendre à une sécurité « totale ». Dites que vous appliquez le principe du moindre privilège et la traçabilité.
> - **Cadre légal des réquisitions**: faites vérifier par vos juristes qui peut requérir, auprès de qui, et sous quel contrôle, avant de le mettre dans le pitch.
> - **Accès à distance**: le jury posera sans doute la question du poste personnel. Préparez la réponse « aucune donnée stockée sur l'appareil, accès révocable ».
>
> Je peux maintenant intégrer ces éléments (sécurité, MFA, hub de réquisitions) dans le brief complet destiné à Claude Code.

## Les deux messages qui ont suivi

> On s’en fiche, oui : on garde Chronos et toutes les promesses, on les met.

> Je vois que tu n’as pas ajouté le niveau sécurité, il faut bien l’ajouter : stocker des données sensibles, relier les différents acteurs sur une plateforme, vraiment vérifier toutes les problématiques et présenter les solutions (pas besoin du site, on l’ignore). Le but est juste de montrer qu’on est sécurisé : double authentification, etc.
