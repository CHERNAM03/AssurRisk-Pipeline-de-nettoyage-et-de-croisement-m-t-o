# Notes d’analyse — enquêtes sur les sinistres

## Fiche 1 — Le dégât des eaux est-il premier dans les 30 villes ?

### 1. Ce qui m’étonne
Dans les 30 villes étudiées, le dégât des eaux est le type de sinistre le plus fréquent.

### 2. Ce que je propose
Je pense que le dégât des eaux est le type le plus fréquent dans chacune des 30 villes, et pas seulement dans le total de la table.

### 3. Ce que je devrais voir
Si mon hypothèse est vraie, le dégât des eaux devrait être seul en tête dans chacune des 30 villes. Si elle est fausse, au moins une ville devrait avoir un autre type en tête ou une égalité.

### 4. Ce que je vois vraiment
Dans l’ensemble de la table, les dégâts des eaux représentent 29,1 % des sinistres, devant le vol (17,5 %). La comparaison ville par ville donne 30 villes sur 30 où le dégât des eaux est seul en tête, aucune égalité et aucune ville où un autre type le devance. Sa part varie de 23,1 % à 34,8 % selon la ville.

### 5. Conclusion et confiance
L’hypothèse est confirmée pour les données étudiées : le dégât des eaux est seul en tête dans chacune des 30 villes. J’ai confiance dans ce constat descriptif, car le classement a été vérifié ville par ville. Cela n’explique pas pourquoi ce type est le plus fréquent.

## Fiche 2 — Pourquoi y a-t-il un pic de sinistres en octobre 2025 ?

### 1. Ce qui m’étonne
Le nombre de sinistres est particulièrement élevé en octobre 2025.

### 2. Ce que je propose
Je pense que le nombre de sinistres a fortement augmenté en octobre 2025 parce que de fortes pluies ont provoqué davantage de dégâts des eaux.

### 3. Ce que je devrais voir
Si cette explication est juste, les dégâts des eaux devraient être plus nombreux lors des fortes pluies, aux mêmes dates et dans les mêmes villes. Si elle ne l’est pas, le pic pourrait être réparti sur d’autres types, dates ou villes, sans relation claire avec la pluie.

### 4. Ce que je vois vraiment
Les données contiennent 1 940 sinistres en octobre, du 1er au 28, soit 69,3 sinistres par jour. C’est la moyenne quotidienne la plus élevée observée; la suivante est 36,7 par jour en février 2025. Les dégâts des eaux représentent 44,8 % des sinistres d’octobre, contre 26,1 % le reste de la période, soit 18,7 points de plus.

Des coïncidences météo-sinistres sont présentes : à Grenoble, le 20 octobre, on observe 44,7 mm de pluie et 6 sinistres. Ce total comprend tous les types de sinistres, pas uniquement les dégâts des eaux. Le tableau des sinistres seuls ne permet pas de comparer correctement les jours-ville sans sinistre.

### 5. Conclusion et confiance
Le pic d’octobre et la part plus élevée des dégâts des eaux sont confirmés dans la table. L’hypothèse d’un rôle des pluies est plausible, mais elle n’est pas démontrée par ces seuls constats. Il faudrait comparer les nombres de sinistres — notamment les dégâts des eaux — aux précipitations pour toutes les villes et dates, y compris les couples ville-date sans sinistre. Confiance élevée dans le constat du pic, mais limitée dans son explication par la météo. Cette analyse ne permet pas de conclure à un lien avec le changement climatique.

## Fiche 3 — Combien de temps s’écoule avant la déclaration ?

### 1. Ce qui m’interroge
Je veux savoir combien de temps s’écoule entre la survenance d’un sinistre et sa déclaration.

### 2. Ce que je propose
Je vais calculer le délai en jours entre `date_survenance` et `date_declaration`, puis comparer ce délai selon le type de sinistre.

### 3. Ce que je devrais voir
Si le délai est similaire quel que soit le type, les moyennes et médianes par type devraient être proches. Si certains types sont déclarés plus vite ou plus tard, leurs délais devraient se distinguer nettement.

### 4. Ce que je vois vraiment
Les 12 098 dossiers ont une date de déclaration. Le délai varie de 1 à 27 jours; il est de 13,9 jours en moyenne et de 14 jours en médiane. Par type, les moyennes vont de 13,5 jours pour la responsabilité civile à 14,4 jours pour l’inondation. Les médianes sont de 14 jours, sauf pour l’inondation (15 jours). Aucune déclaration n’a lieu le jour même ou avant la survenance.

### 5. Conclusion et confiance
Les délais sont proches entre les types de sinistre dans les dossiers étudiés; je ne vois pas de grande différence descriptive. J’ai confiance dans les statistiques calculées sur cette table, mais elles ne permettent pas d’expliquer les délais ni de généraliser à d’autres dossiers.

## Ce que la météo n’explique pas : trois corrélations à examiner

Une corrélation mesure une association entre deux variables; elle ne prouve pas qu’une variable cause l’autre. Les résultats numériques de ces trois corrélations ne figurent pas dans les sorties déjà disponibles : ils restent à calculer avant de les rapporter.

1. **Précipitations et nombre total de sinistres** par ville et par jour d’octobre. Cela vérifie si les jours plus pluvieux coïncident avec plus de sinistres, tous types confondus.
2. **Précipitations et nombre de dégâts des eaux** par ville et par jour d’octobre. C’est le test le plus directement lié à l’hypothèse de fortes pluies.
3. **Rafales maximales et nombre de sinistres Tempête** par ville et par jour d’octobre. Cela examine une autre association météo-sinistre pertinente.

