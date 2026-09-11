# Décimales, échelles et arrondis

Un prix n’est interprétable qu’avec son échelle. L’adaptateur doit normaliser la valeur source vers le nombre de décimales annoncé et protéger les multiplications contre les dépassements ou pertes de précision.

Un facteur erroné de dix peut déclencher des liquidations ou autoriser un emprunt sous-collatéralisé. Le consommateur devrait vérifier decimals lors de l’intégration et ne pas supposer qu’il vaut toujours huit.

Les conversions entre entiers signés et non signés demandent une validation explicite. Une valeur nulle ou négative doit être rejetée avant toute conversion qui en modifierait le sens.

L’arrondi devrait être choisi selon le risque : valorisation prudente du collatéral et dette non sous-estimée. Cette règle doit rester cohérente entre l’oracle, le marché et les calculs de santé.

[Chapitre suivant : keepers et EMA](05-keepers-et-ema.md)
