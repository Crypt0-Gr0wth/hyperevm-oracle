# Confiance et temporalité inter-couches

Le chemin perpétuel dépend des prix acceptés par les validateurs Hyperliquid L1 puis rendus accessibles à HyperEVM. Cette traversée ajoute une hypothèse de disponibilité et une différence possible entre temps source et temps d’exécution.

Un protocole de prêt ne doit pas confondre finalité d’un bloc HyperEVM et actualité économique du prix. Une transaction peut être finale tout en consommant une observation trop ancienne pour le niveau de volatilité courant.

Les scénarios de partition, de retard et de marché suspendu doivent avoir une réponse déterministe. Le comportement le plus sûr est souvent de bloquer les nouvelles prises de risque tout en préservant les opérations de remboursement.

La surveillance devrait comparer âge réel de la source, variation entre observations et disponibilité du chemin L1. Une simple réussite de l’appel ne suffit pas comme signal de santé.

[Chapitre suivant : surface de production](07-proxy-et-surface-de-production.md)
