# 03 — Projets pratiques

Objectif : comprendre en fabriquant.

## P0 — Bandit + GridWorld

**But :** réactiver le RL.

Livrables :
- bandit multi-bras ;
- GridWorld ;
- Q-learning ;
- graphiques reward / exploration.

Ne pas sur-ingénier.

---

## P1 — Coordination Game avec PettingZoo

**But :** sentir ce qui rend le MARL différent.

Faire deux agents dans un jeu où ils doivent choisir des actions compatibles.

Variantes :
- reward commun ;
- reward individuel ;
- observations partielles ;
- même policy partagée ;
- policies indépendantes.

Questions :
- apprennent-ils la même convention à chaque seed ?
- deux agents entraînés séparément peuvent-ils coopérer ?

---

## P2 — Costly Communication

**But :** reprendre ton ancien projet sous une forme minimale et mesurable.

Deux agents doivent coopérer avec information distribuée.

Ils disposent d'un canal discret payant.

\[
reward = task\_reward - \lambda \cdot messages
\]

Sweep sur \(\lambda\).

Ablations :
- désactiver les messages ;
- permuter leur sens ;
- injecter du bruit ;
- réduire la bande passante ;
- changer de partenaire.

Ce projet est probablement le premier à mériter un repo expérimental séparé si l'idée devient riche.

---

## P3 — Topology Lab

**But :** étudier le groupe plutôt que seulement les individus.

Population de policies / DQN partageant de l'expérience.

Topologies :
- fully connected ;
- ring ;
- small-world ;
- dynamic.

Mesures :
- performance ;
- diversité ;
- vitesse de propagation d'une stratégie ;
- innovation ;
- effondrement prématuré vers un consensus.

Inspiré de SAPIENS, sans chercher d'abord une reproduction exacte.

---

## P4 — Zero-Shot Partner Swap

**But :** mesurer ce qui dépend d'une histoire partagée.

Former des paires / groupes séparément.

Puis :
- échanger les partenaires ;
- insérer une copie neuve ;
- insérer un agent entraîné indépendamment ;
- tester des conventions compatibles / incompatibles.

Question :
> Que reste-t-il de la coordination lorsque l'histoire commune disparaît ?

---

## P5 — Same Brain, Different Bodies

**But :** tester ton intuition initiale sous une forme propre.

Plusieurs agents utilisent exactement la même policy / mêmes poids mais :
- observations différentes ;
- mémoires locales séparées ;
- positions / corps différents.

Comparer avec :
- poids différents ;
- seeds différents ;
- fine-tunes différents.

Mesurer :
- coordination zero-shot ;
- interchangeabilité des rôles ;
- spécialisation ;
- robustesse au remplacement.

---

## P6 — Similarity Sweep

**But :** transformer "homogeneous" en variable causale.

Échelle progressive :
- mêmes poids ;
- mêmes poids + histoires différentes ;
- mêmes poids initiaux + fine-tunes ;
- même famille ;
- familles distinctes.

Ne pas utiliser cette échelle comme vérité théorique : elle doit être raffinée.

Question :
> Existe-t-il un compromis entre priors partagés et diversité complémentaire ?

---

## P7 — Collective Cognition Probe

**But :** approcher la question de recherche elle-même.

Tâche nécessitant plusieurs informations distribuées.

Chercher une situation où :
- aucun agent seul ne dispose de l'information suffisante ;
- le groupe peut résoudre la tâche ;
- le succès ne peut pas être expliqué par un simple vote / ensemble trivial.

Ablations :
- supprimer un agent ;
- casser le canal ;
- mélanger les identités ;
- remplacer un agent par un clone ;
- remplacer par un modèle différent.

---

## P8 — Riedl Minimal Replication

**But :** comprendre réellement son cadre.

Commencer sans PID sophistiquée :
- reproduire le jeu ;
- reproduire les conditions ;
- regarder rôles / complémentarité / stabilité.

Ajouter ensuite les métriques informationnelles.

---

## Capstone — Collective Cognition Sandbox

Un seul environnement configurable pour expérimenter sur :
- similarité des agents ;
- mémoire ;
- topologie ;
- coût de communication ;
- taille de population ;
- reward structure ;
- remplacement des membres ;
- noise ;
- feedback collectif.

Ne commencer ce capstone qu'après P2–P5. Sinon tu risques de construire une infrastructure avant d'avoir une question.
