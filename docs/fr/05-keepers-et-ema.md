# Keepers et moyenne mobile exponentielle

Les actifs sans marché perpétuel dépendent de prix soumis par des keepers puis lissés par une moyenne mobile exponentielle. L’EMA réduit certains à-coups, mais elle introduit une mémoire et un retard propres.

La sécurité dépend de l’autorisation des keepers, de leur diversité et des bornes imposées à chaque observation. Un keeper compromis ne devrait pas pouvoir déplacer instantanément le prix au-delà d’un seuil raisonnable.

Il faut définir le comportement lorsque trop peu de sources répondent : geler, refuser la valeur ou passer dans un mode de secours explicite. Réutiliser indéfiniment la dernière observation transforme une panne en prix trompeur.

Les paramètres de l’EMA sont économiques autant que techniques. Une fenêtre lente résiste mieux aux pointes mais peut retarder une liquidation légitime pendant un marché violent.

[Chapitre suivant : confiance inter-couches](06-confiance-inter-couches.md)
