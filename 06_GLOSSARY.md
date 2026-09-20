# 06 — Glossaire minimal

## RL — Reinforcement Learning
Apprentissage où un agent agit dans un environnement et optimise des récompenses cumulées.

## MARL — Multi-Agent Reinforcement Learning
RL avec plusieurs agents en interaction dans un même environnement.

## MDP — Markov Decision Process
Formalisation d'un problème de décision séquentielle où l'état courant contient l'information pertinente pour la dynamique future.

## POMDP
MDP partiellement observable : l'agent ne voit pas directement tout l'état.

## Policy
Règle / modèle qui associe observations ou états à des actions.

## Value function
Estimation du return futur attendu depuis un état.

## Q-function
Valeur attendue d'une action dans un état, suivie de la politique considérée.

## Self-play
Entraînement d'un agent principalement contre / avec des copies ou versions de lui-même.

## Non-stationarity
En MARL, le comportement des autres agents change pendant l'apprentissage ; l'environnement vu par chaque agent n'est donc plus stationnaire.

## CTDE
Centralized Training, Decentralized Execution. L'entraînement peut utiliser des informations globales, mais chaque agent agit ensuite avec ses informations locales.

## Parameter sharing
Plusieurs agents utilisent les mêmes paramètres de policy, éventuellement avec observations / identités locales différentes.

## Emergent communication
Protocole de communication appris par les agents plutôt que fixé entièrement par le concepteur.

## Zero-shot coordination
Capacité à coopérer avec un partenaire jamais rencontré pendant l'entraînement.

## Social generalization
Capacité à généraliser à de nouveaux partenaires / comportements sociaux.

## Autocurriculum
Processus où les nouvelles stratégies des agents créent elles-mêmes de nouveaux défis d'apprentissage.

## Autotelic agent
Agent capable de générer / sélectionner ses propres objectifs plutôt que de suivre uniquement un objectif externe fixé.

## Collective intelligence
Capacité ou performance apparaissant au niveau d'un groupe d'agents en interaction.

## Distributed cognition
Perspective où certains processus cognitifs sont portés par un système de plusieurs composants plutôt que par un seul individu.

## Synergy
Information / contribution utile qui apparaît dans la combinaison de plusieurs sources et n'est pas disponible dans chacune séparément.

## Redundancy
Information similaire ou dupliquée présente dans plusieurs sources.

## Mutual information
Mesure informationnelle de la dépendance entre deux variables.

## PID — Partial Information Decomposition
Famille de méthodes qui décompose l'information apportée par plusieurs sources en contributions uniques, redondantes et synergiques.

## Ablation
Expérience où l'on retire ou perturbe un composant afin de tester son rôle causal.

## Network topology
Structure du graphe décrivant qui peut interagir avec qui.

## Small-world network
Réseau combinant clustering local relativement fort et chemins courts entre nœuds.

## Consensus
Convergence des agents vers une même croyance / action / convention. Un consensus n'est pas automatiquement une preuve d'intelligence collective.
