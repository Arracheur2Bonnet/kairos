# Pistes explorées

Ce que l’équipe a essayé pendant le hackathon, ce qui est resté, ce qui a été écarté et pourquoi. Chaque piste dit où la retrouver dans le dépôt. Les prototypes et présentations d’époque sont dans [les archives](../archives/README.md).

| Piste | Sort | Où la retrouver |
|---|---|---|
| Tour de contrôle des procédures (idée de départ) | Resserrée sur l’information de la victime | [texte d’origine](../archives/textes-d-origine/01-idee-de-depart.md) |
| Vérification des pièces et des mentions (« scanner de vigilance ») | **Gardée** : première fonction de Kairos | Onglet Vigilance du prototype |
| Alertes plutôt que notes | **Gardée** | Prototype, pilotage |
| Frise des demandes de libération, sorties, avis à la victime, convocations | Gardée dans le prototype | Onglet Affaire |
| Rapprochement d’affaires (escroquerie : même téléphone, même compte, même domaine) | Retiré le 15 octobre à 14 h 08 à la demande de l’équipe | Prototypes v02 à v05 |
| Victime qui déménage, avec contrôle de la zone d’interdiction | Dans le prototype, hors pitch | Prototype, bloc « Protection de Mme M. » |
| Cycle de vie des alertes (prise en charge, escalade, compte à rebours, alertes d’absence) | Dans le prototype, hors pitch | Onglet Vigilance |
| Fiabilité des données et croisements officiels (impôts, état civil) | Dans le prototype, hors pitch | Données de l’affaire |
| Assistant de questions | Dans le prototype, hors pitch (il contredit « les autres IA répondent, la nôtre s’assure que l’information est arrivée ») | Bouton « Demander à Kairos » |
| Circulation d’une décision (destinataires, accusés, relance à 24 h, mesure) | Abandonnée par l’équipe (« trop éloignée »), mais le cœur de Kairos y ressemble | [archives/chronos-circulation](../archives/chronos-circulation/) |
| « Chronos comme source » (même personne dans deux procédures) | Abandonnée avec la version circulation | Même dossier |
| Réquisitions interservices | Non retenue : hors périmètre | [texte d’origine](../archives/textes-d-origine/05-conception-securite-interservices.md) |
| Briques Microsoft | Piste d’architecture, non arrêtée | ci-dessous |

## La victime qui déménage

Idée de l’équipe : si la personne protégée déménage, vérifier qu’elle reste protégée. Version construite : une « carte de protection » visible seulement du parquet, du juge de l’application des peines et du juge aux affaires familiales, sans jamais afficher d’adresse (seulement des communes et des distances). Un événement « Mme M. déménage à Corbelle » déclenche quatre contrôles : masquer la nouvelle adresse partout, vérifier si les interdictions couvrent encore la nouvelle commune (ici, l’interdiction de paraître vise Valmont : « à examiner par le juge », car lui seul peut la modifier), vérifier l’inscription des interdictions au fichier des personnes recherchées (article 230-19 du CPP, qui y fait inscrire les obligations du contrôle judiciaire et, depuis 2016, les interdictions de l’ordonnance de protection), et croiser avec l’adresse de sortie de l’auteur déclarée au service pénitentiaire. Le texte précise que si l’auteur est inscrit au FIJAIS, chaque changement d’adresse qu’il déclare est croisé de la même façon.

Écartée du pitch parce que la base légale de ces croisements n’est pas établie. Corrections apportées en route : la « fiche S » est une catégorie du fichier des personnes recherchées réservée à la sûreté de l’État, sans rapport avec les violences conjugales et inaccessible à un greffe ; pas de géolocalisation en temps réel (c’est le rôle du bracelet, un système à part). À vérifier : l’inscription au fichier des personnes recherchées d’une interdiction de paraître prononcée hors contrôle judiciaire ; les règles du FIJAIS (issues d’un blog d’avocat).

## Les alertes comme produit

Une bonne alerte répond à sept questions : quoi, pourquoi (explication de l’IA), d’après quelle source, qui doit agir, avant quand, que faire en un clic, et ce que Kairos n’a pas fait. Les **alertes d’absence** signalent ce qui aurait dû se produire et ne s’est pas produit (accusé de réception non revenu, avis à la victime non envoyé avant une sortie, avis au procureur introuvable pendant une garde à vue, pièce annoncée mais absente) : aucun logiciel actuel ne les voit, parce que chacun ne regarde que ses propres données. Cycle de vie : créée, vue, prise en charge, résolue avec un motif ; escalade automatique si personne ne la prend (garde à vue : au bout de 30 minutes, au magistrat de permanence) ; compte à rebours pour les délais légaux ; routage vers un rôle plutôt qu’une personne ; une seule alerte par situation ; un retour « utile / pas utile » qui ajuste les règles et jamais n’évalue les agents.

## Fiabilité des données et impôts

Idée : utiliser les données de l’administration fiscale pour l’authenticité et la fraîcheur des informations. L’API « Impôt particulier » de la DGFiP, accessible par Datapass, fournit revenu fiscal de référence, parts, situation de famille et adresse fiscale, sous secret fiscal et avec une base légale à cadrer. Usages explorés : authentifier un avis d’imposition versé au juge aux affaires familiales (pension, aide juridictionnelle), repérer une adresse périmée (jamais pour faire apparaître une adresse protégée), afficher un niveau de fiabilité par donnée, en catégories et sans score : « certifiée par la source », « vérifiée auprès d’une source officielle » (impôts, état civil par COMEDEC), « déclarative ». Même logique avec les allocations familiales pour l’intermédiation des pensions. Phrase de pitch d’époque : « Chronos ne se contente pas de relier les informations : il dit lesquelles sont certifiées. » Écartée du pitch, base légale non établie.

## « Chronos comme source » et le rapprochement

Variante essayée dans la version circulation : un signal « M. Julien R. serait aussi mis en cause dans une plainte à Corbelle », fondé sur quatre éléments d’identité concordants sur quatre, sans score, sans affirmation, avec proposition de transmettre aux parquets ou d’écarter un homonyme. Analyse de l’équipe de travail : l’idée est bonne en principe, mais « mise en cause » est une qualification de la procédure pénale réservée aux enquêteurs, au parquet et au juge ; un outil de greffe qui l’établit désigne un auteur, ce qui contredit « il n’évalue aucune personne » et la présomption d’innocence. Les rapprochements judiciaires sont encadrés (articles 230-20 et suivants du CPP) : ne pas dire que c’est autorisé, dire qu’il faudra l’examiner avant tout usage réel. Les simulations ne prouvent rien sur la performance : ne jamais citer un taux de réussite obtenu sur des données simulées.

## Briques Microsoft envisagées

Pistes, pas une architecture arrêtée ; l’hébergement et les services restent à fixer avec le ministère, sous exigence de souveraineté.

| Besoin | Brique envisagée |
|---|---|
| Lire les PV et décisions (PDF, scans) | Azure AI Document Intelligence |
| Extraire, vérifier, rédiger le message ; expliquer les alertes | Azure OpenAI, dans Azure AI Foundry |
| Retrouver les dossiers liés à une même personne | Azure AI Search |
| Brancher les logiciels existants | API Management, Logic Apps, Event Grid |
| Validation du greffe, alertes | Application web ; notifications Teams ou Outlook via Power Automate (validations dans Teams) |
| Traçabilité (source, auteur, version) | Dataverse, Microsoft Purview |
| Identités et droits | Microsoft Entra ID |

Conseil donné pendant le hackathon : un seul bloc réellement branché en direct (de quelques faux PDF jusqu’à l’alerte sourcée puis à la validation) vaut mieux que cinq écrans simulés. Dans le prototype, tout est simulé.
