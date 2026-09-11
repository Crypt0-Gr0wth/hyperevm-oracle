# Compatibilité d’interface et équivalence sémantique

AssetOracleProxy expose notamment latestAnswer et latestRoundData afin de faciliter l’intégration avec des consommateurs conçus pour Chainlink. Une signature identique ne garantit pourtant pas des champs de même sens.

Les consommateurs utilisent souvent roundId, answeredInRound et updatedAt pour vérifier qu’une ronde est complète et suffisamment récente. Si ces champs sont synthétiques, les contrôles hérités peuvent devenir inopérants sans erreur visible.

Chaque adaptateur devrait documenter précisément la source, l’unité, le nombre de décimales et la signification de chaque champ retourné. Le contrat consommateur doit valider ces garanties, pas seulement réussir l’appel.

Une intégration sûre traite donc l’interface comme un format de transport. Le modèle de confiance reste celui de l’oracle HyperEVM sous-jacent.

[Chapitre suivant : fraîcheur](03-fraicheur-et-horodatage.md)
