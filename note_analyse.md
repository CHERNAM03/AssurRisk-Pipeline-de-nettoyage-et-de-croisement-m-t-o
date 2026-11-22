# Note d’analyse — sinistres et météo

## Partie 1 — Le montant d’un sinistre
- Observation : le montant estimé varie de 80 € à 49 912 € dans les données étudiées.
- Explication proposée : les montants peuvent varier selon le type et l’ampleur des dommages.
- Vérification : `describe()` donne les minimum et maximum; les moyennes et médianes ont aussi été comparées par type de sinistre.
- Conclusion : les montants sont très hétérogènes; ces statistiques descriptives ne suffisent pas à expliquer les écarts.
- Confiance : élevée pour les valeurs observées dans la table, limitée pour leur explication.

## Partie 2 — Le type de sinistre le plus fréquent
- Observation : les dégâts des eaux représentent 29,1 % des sinistres, devant le vol à 17,5 %.
- Explication proposée : ce type pourrait être fréquent dans toutes les villes, et pas seulement dans celles qui comptent le plus de dossiers.
- Vérification : un classement par ville confirme que les dégâts des eaux sont seuls en tête dans les 30 villes, sans égalité.
- Conclusion : l’hypothèse est confirmée pour les 30 villes étudiées; cela n’explique pas la cause de cette fréquence.
- Confiance : élevée pour ce constat descriptif, vérifié ville par ville.

## Partie 3 — Octobre 2025
- Observation : 1 940 sinistres sont recensés du 1er au 28 octobre, soit 69,3 par jour, la moyenne quotidienne la plus élevée de la période.
- Explication proposée : de fortes pluies pourraient avoir contribué au pic, notamment en augmentant les dégâts des eaux.
- Vérification : les dégâts des eaux représentent 44,8 % des sinistres en octobre contre 26,1 % le reste de la période; à Grenoble, le 20 octobre, 44,7 mm de pluie coïncident avec 6 sinistres.
- Conclusion : le pic est établi, mais ces coïncidences ne démontrent pas que la pluie l’a causé et ne permettent pas de conclure à un lien avec le changement climatique.
- Confiance : élevée pour le constat du pic, limitée pour son explication météorologique.

## Partie 4 — Ce que la météo n’explique pas
- Observation : les trois corrélations de Pearson calculées par ville et par jour d’octobre sont proches de zéro.
- Explication proposée : dans ces données, la pluie ou les rafales ne semblent pas expliquer à elles seules les variations quotidiennes du nombre de sinistres.
- Vérification : pluie/tous les sinistres : r = -0,039; pluie/dégâts des eaux : r = -0,042; rafales/sinistres Tempête : r = 0,053.
- Conclusion : ces résultats ne montrent pas de relation linéaire marquée entre les paires de variables examinées.
- Confiance : modérée pour ces associations descriptives; elles ne prouvent ni causalité ni absence de tout autre lien.
