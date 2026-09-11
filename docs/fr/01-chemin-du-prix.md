# Du système oracle Hyperliquid à HyperEVM

Le dépôt expose sur HyperEVM des prix issus de deux chemins. Lorsqu’un actif possède un marché perpétuel, le prix provient du System Oracle de Hyperliquid, alimenté par les validateurs de la couche L1.

Pour les autres actifs, des keepers soumettent des observations et l’oracle calcule une moyenne mobile exponentielle. Les deux chemins aboutissent à une interface proche de Chainlink, mais leurs hypothèses de confiance ne sont pas identiques.

Un consommateur doit savoir quel chemin a produit la valeur. Sans cette information, il ne peut pas appliquer une politique de fraîcheur, de dégradation ou de liquidation adaptée.

La compatibilité applicative simplifie l’intégration. Elle ne doit pas effacer la provenance du prix ni le modèle de sécurité qui lui est associé.

[Chapitre suivant : compatibilité Chainlink](02-compatibilite-chainlink.md)
