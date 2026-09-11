# Fraîcheur et horodatage

La documentation indique que, pour les actifs perpétuels, roundId et answeredInRound valent zéro tandis que startedAt et updatedAt correspondent à block.timestamp. Ce choix mérite une attention particulière.

block.timestamp décrit l’instant de lecture sur HyperEVM, pas nécessairement l’instant où le prix source a été observé ou accepté par les validateurs. Un contrôle de staleness fondé sur ce champ peut donc accepter une valeur ancienne comme récente.

Le consommateur devrait disposer d’un horodatage de source ou d’un identifiant d’observation monotone. À défaut, il doit appliquer une politique conservatrice fondée sur les garanties réelles du System Oracle.

Il faut aussi distinguer absence de mise à jour, retard inter-couches et arrêt du marché. Ces états ne devraient pas tous produire silencieusement une valeur apparemment fraîche.

[Chapitre suivant : décimales](04-decimales-et-arrondis.md)
