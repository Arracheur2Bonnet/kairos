# Le dossier rédigé

Copie texte de [Kairos-dossier-redige.pdf](../Kairos-dossier-redige.pdf), pages 1 et 2. Le PDF fait foi : cette copie sert à chercher dans le texte, à le citer et à ne pas le perdre. Les mots coupés en fin de ligne ont été recollés, la typographie française rétablie ; les mots sont ceux du PDF, y compris deux petites maladresses relevées dans [les points de vigilance](points-de-vigilance.md). **Une différence voulue :** « Un homme détenu pour violences conjugales demande sa mise en liberté » (le PDF dit « condamné », voir [les points de vigilance](points-de-vigilance.md)). Le texte du pitch (pages 3 et 4) est dans [pitch.md](pitch.md).

---

# Kairos

*Le suivi de colis de la justice*

## Le contexte

Cassiopée est le traitement informatique des tribunaux judiciaires, créé par l’article 48-1 et les articles R. 15-33-66-4 et suivants du code de procédure pénale. Selon la CNIL, il enregistre les plaintes et dénonciations reçues par les magistrats et accompagne toute la vie de la procédure (audiences, décisions, voies de recours, exécution des peines) « afin d’améliorer le délai de traitement des procédures, et d’assurer l’information des victimes ». L’information des victimes fait donc déjà partie de sa raison d’être. Cassiopée n’est cependant qu’un maillon d’une chaîne plus large : une même affaire passe aussi par le logiciel civil du juge aux affaires familiales, par celui de l’administration pénitentiaire, par ceux de la police. Ces outils ont été conçus séparément et communiquent mal entre eux.

Il en résulte trois difficultés, que l’Inspection générale de la justice décrit dans son rapport de décembre 2025 consacré au traitement judiciaire des violences intrafamiliales : des données saisies plusieurs fois et donc fragiles, une charge administrative lourde pour les greffes, et des informations qui ne circulent pas d’un service à l’autre. Le dossier commun créé pour ces affaires, SISPoPP, reste peu utilisé, précisément parce qu’il faut tout y ressaisir.

## Le problème

Ces difficultés pèsent d’abord sur les victimes. Une décision qui touche à leur sécurité (la sortie de prison de l’auteur, sa remise en liberté, l’annulation de leur protection en appel) doit leur être notifiée. La loi l’impose. Mais l’information dépend de chaque tribunal et de la vigilance de chacun.

Les chiffres de l’Inspection générale de la justice le montrent : lorsque l’auteur sort en fin de peine, 95 % des tribunaux préviennent la victime ; lorsque la cour d’appel annule une ordonnance de protection, ils ne sont plus que 55 %. Plus une décision traverse de services, moins elle arrive. Et dans aucun cas on ne sait si la victime a réellement reçu l’information.

*Comment garantir que chaque décision qui touche une victime lui parvienne au bon moment, et le prouver ?*

## Notre solution

Kairos est une brique d’intelligence artificielle complémentaire à Cassiopée : il rend effective une mission que Cassiopée porte déjà, l’information des victimes, en la prolongeant au-delà de ses murs et en apportant la preuve qu’elle a été remplie. Elle ne remplace aucun logiciel existant : elle s’y branche, pour rendre le suivi des procédures plus fiable, plus fluide et plus sûr. Proposée sous la forme d’une application web hébergée dans un cloud souverain, elle repose sur trois axes.

**Analyser les pièces.** L’intelligence artificielle lit les procès-verbaux des enquêteurs et les décisions des juges. Elle en extrait les personnes, leurs adresses et téléphones, les dates et les mesures prononcées. Elle vérifie les mentions obligatoires de chaque acte et les éléments qui conditionnent sa validité : une notification absente, une adresse ancienne, un numéro manquant, un délai qui approche. Elle alerte le professionnel des risques identifiés, et c’est lui qui apprécie.

**Relier les services.** Des connecteurs font circuler l’information entre Cassiopée, les logiciels civils, pénitentiaires et policiers. Des règles juridiques indiquent, pour chaque type de décision, qui doit en être informé et en vertu de quel texte. Une information saisie une fois devient connue de tous ceux qui en ont besoin.

**Notifier automatiquement et prouver.** La notification est automatisée : Kairos rédige le message en mots simples et l’envoie lui-même, dès que le greffe a validé d’un clic. Il suit ensuite chaque envoi, comme on suit un colis : envoyé, reçu, lu. Si la victime n’a rien reçu à temps, le greffe est alerté.

## Un exemple concret

Un homme détenu pour violences conjugales demande sa mise en liberté. Kairos intervient dès la demande, avant toute sortie : il ouvre le dossier et compare les éléments. L’intelligence artificielle retrouve la victime, vérifie son adresse et son dernier numéro de téléphone, et rappelle l’interdiction de contact toujours en vigueur. La victime est ainsi prévenue en amont, et non le jour où elle le croise. Si la liberté est accordée, Kairos affiche les personnes à prévenir : la victime, son avocate, le commissariat de son quartier. Le greffier valide, et le message part automatiquement : « Il sort le 20 octobre. Il n’a pas le droit de vous contacter. En danger, appelez le 17. » Si elle n’a pas lu le message la veille de la sortie, le greffe est alerté et l’appelle.

## Les garanties

Kairos ne prend aucune décision : chaque envoi est validé par un agent du greffe. Il n’évalue aucune personne. Chaque action est journalisée. Les adresses successives de la victime sont conservées avec leur date et leur source ; le téléphone est privilégié, et une confirmation est demandée au moindre doute, car un message mal adressé peut être plus dangereux qu’un message absent. L’outil reste interne à l’État et respecte le secret de l’enquête et la protection des données.

## La portée et la demande

Kairos commence par les victimes de violences conjugales, là où l’enjeu est le plus grave. Mais le même moteur vaut pour l’ensemble des procédures judiciaires : pour toute décision qui doit parvenir à quelqu’un, et pour la fiabilité de chaque procédure, dont il vérifie les étapes et les délais : notre analyse de 440 000 décisions de cours d’appel montre que plus de 12 000 appels ont été arrêtés depuis 2022, souvent pour un délai manqué. Nous proposons un pilote de six mois dans un tribunal : trois mois pour mesurer la situation actuelle, trois mois pour mesurer l’effet de Kairos.

*Sources.* CNIL, fiche « CASSIOPEE : Chaîne applicative supportant le système d’information orienté procédure pénale et enfants » (textes : art. 48-1 et R. 15-33-66-4 et s. du code de procédure pénale ; délibération CNIL n° 2009-170 du 26 mars 2009), https://www.cnil.fr/fr/cassiopee-chaine-applicative-supportant-le-systeme-dinformation-oriente-procedure-penale-et-enfants. Inspection générale de la justice, *Évaluation du traitement judiciaire des violences intrafamiliales*, rapport définitif n° 073-25, décembre 2025, enquête auprès de 152 tribunaux judiciaires (déclaratif) : 95,4 % des tribunaux informent la victime d’une libération en fin de peine (p. 52), 55,3 % d’une ordonnance de protection infirmée en appel (p. 45) ; usage limité de SISPoPP (p. 4) ; ressaisie des dossiers (p. 49). Judilibre, open data de la Cour de cassation : 440 460 décisions de cours d’appel analysées par l’équipe (janvier 2022 à septembre 2026), 12 371 appels déclarés caducs, lecture vérifiée à la main (23 justes sur 24). Test du concept avec un expert le 15 octobre 2026. Démonstration sur données fictives.
