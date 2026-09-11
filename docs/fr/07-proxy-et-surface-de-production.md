# Proxy, agrégateur et surface de production

Le dépôt précise que Aggregator.sol n’est pas utilisé en production, tandis que AssetOracleProxy fournit l’interface consommée. Cette distinction évite d’attribuer à l’architecture déployée des propriétés visibles seulement dans un contrat expérimental.

L’analyse doit suivre l’adresse réellement configurée par le marché : proxy, implémentation, administrateur et source de prix. Un contrat présent dans le dépôt n’est pas nécessairement une dépendance active.

Si une mise à niveau ou un changement de source est possible, son autorité et son délai font partie du modèle de risque. Un changement instantané peut corriger une panne, mais aussi modifier les garanties sans délai pour les emprunteurs.

Les intégrateurs devraient épingler les paramètres attendus et surveiller les événements d’administration. Toute divergence doit suspendre les opérations sensibles jusqu’à vérification.

[Chapitre suivant : intégration défensive](08-integration-defensive.md)
