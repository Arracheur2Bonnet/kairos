# Données de l’Inspection générale de la justice

Texte du 15 octobre 2026, 14 h 58. L’équipe colle un extrait du rapport de l’Inspection générale de la justice (IGJ) sur le traitement judiciaire des violences intrafamiliales et demande de le vérifier et de l’ajouter. Ces cinq pourcentages sont devenus le constat du pitch : 95 % quand l’auteur sort en fin de peine, 55 % quand la cour d’appel annule l’ordonnance de protection.

## Le message de l’équipe

> Vérifie et ajoute ces données qu’on peut donner pour notre cas :

## L’extrait collé, tel quel

Les retours à la ligne au milieu des phrases viennent de la copie depuis le PDF.

```text
ttps://www.justice.gouv.fr/sites/default/files/2026-03/rapport_mission_igi_vif.pdf
Évaluation du traitement judiciaire des violences intrafamiliales - Rapport définitif 12/2025
Si la mission constate que l'information de la victime à tous les stades de la procédure a largement progressé dans les pratiques, notamment sous la pression des évolutions textuelles, elle relève toutefois que certaines situations mériteraient un surcroît
95,4 % des
T ont indiqué informer systématiquement
et immédiatement la victime en cas de libération de l'auteur de VIF à l'issue de l'exécution
de sa peine. Ce taux s'établit à 86,2 % en cas de libération dans le cadre d'une permission de sortir et à 79,6 % en cas de remise en liberté au stade de la détention provisoire.
En revanche, seuls 59,2 % des TJ ont indiqué informer la victime en cas de refus de placement en détention provisoire, ce qui peut surprendre immédiatement après le défèrement de l'auteur118
. Enfin, seuls 55,3 % des TJ ont répondu ne pas informer
la victime en cas d'infirmation par la CA de l'OP délivrée par le TJ119
```

Le lien collé commençait par « ttps » (le « h » manquait) et se terminait par « igi_vif.pdf ».

## Ce que nous en avons tiré

| Situation | Part des tribunaux judiciaires (TJ) | Formulation de l’extrait |
|---|---|---|
| Libération de l’auteur à l’issue de sa peine | 95,4 % | « ont indiqué informer systématiquement et immédiatement la victime » |
| Libération dans le cadre d’une permission de sortir | 86,2 % | « Ce taux s’établit à 86,2 % » |
| Remise en liberté au stade de la détention provisoire | 79,6 % | « et à 79,6 % » |
| Refus de placement en détention provisoire | 59,2 % | « seuls 59,2 % des TJ ont indiqué informer la victime » (note 118) |
| Infirmation par la cour d’appel de l’ordonnance de protection délivrée par le TJ | 55,3 % | « seuls 55,3 % des TJ ont répondu ne pas informer la victime » (note 119) |

## Deux points à vérifier

**Le sens du dernier chiffre.** Lue à la lettre, la dernière phrase dit que 55,3 % des tribunaux *n’informent pas* la victime, ce qui serait le pire résultat de la liste. Lue dans son contexte, elle dit plus probablement que 55,3 % *informent* : la phrase précédente introduit une série de taux d’information décroissants avec « seuls 59,2 % des TJ ont indiqué informer la victime », et la série 95,4, 86,2, 79,6, 59,2, 55,3 est elle-même décroissante. Le dossier, le pitch, les diapositives et le README retiennent « informent ». Le prototype a longtemps affiché l’inverse. Le texte du rapport (page de la note 119) reste à relire, voir [les points de vigilance](../../docs/points-de-vigilance.md).

**Le lien et le numéro.** Le fichier du rapport définitif s’appelle `rapport_mission_igj_vif.pdf` (« igj », et non « igi »), rangé dans le dossier de mars 2026 de justice.gouv.fr d’après l’adresse du fichier : `https://www.justice.gouv.fr/sites/default/files/2026-03/rapport_mission_igj_vif.pdf`. Une recherche web du 16 octobre 2026 l’identifie comme le rapport définitif n° 073-25, décembre 2025, *Évaluation du traitement judiciaire des violences intrafamiliales*. Il existe aussi un rapport d’étape (n° 065-25, novembre 2025), à ne pas confondre. Le site du ministère était en maintenance les 15 et 16 octobre : nous n’avons pas pu ouvrir le PDF, et les pourcentages ci-dessus sont ceux du texte collé.
