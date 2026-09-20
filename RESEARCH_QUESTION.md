# RESEARCH_QUESTION — document vivant

## Version 0 — intuition

Plusieurs instances d'agents très similaires donnent parfois l'impression de fonctionner comme "une même intelligence dans plusieurs corps".

Cette formulation est intuitive, pas scientifique.

## Version 1 — question générale

> **Under what conditions does a population of artificial agents become a collective cognitive system rather than merely a collection of independent agents?**

Cette question reste la boussole.

## Attention

Ne pas décider à l'avance qu'un "collective cognitive system" existe.

Il faut précisément construire des critères permettant :
- de détecter éventuellement ce phénomène ;
- ou de conclure que certaines observations s'expliquent sans cognition collective.

## Version 2 — axe expérimental possible

> **What causal role does agent similarity play in the emergence of collective cognition?**

## Version 3 — formulation plus mécaniste

> **How do shared priors, representations and training histories shape the emergence of collective cognition in populations of artificial agents?**

Ces formulations ne sont pas encore un sujet de thèse final.

---

# Hypothèses candidates à tester, pas à croire

## H1 — Shared priors
Des agents partageant fortement leurs priors peuvent coordonner plus facilement sans communication explicite.

## H2 — Diversity benefit
Une trop forte homogénéité peut réduire la complémentarité et provoquer un consensus prématuré.

## H3 — Intermediate optimum
Il peut exister une zone intermédiaire où suffisamment de structure est partagée pour coordonner, mais suffisamment de diversité subsiste pour produire de la synergie.

## H4 — History vs weights
Une partie de l'effet "hive mind" peut provenir des poids / priors partagés, une autre de l'histoire commune.

## H5 — Distributed state
Certaines capacités peuvent dépendre d'un état informationnel réellement distribué entre agents plutôt que de la seule puissance individuelle.

---

# Variables possibles

## Similarité
- même architecture ;
- mêmes poids ;
- même checkpoint ;
- même teacher / distillation ;
- même corpus partiel ;
- même instruction ;
- même histoire ;
- mêmes représentations.

## Interaction
- aucune communication ;
- observation du comportement ;
- canal discret ;
- langage naturel ;
- mémoire commune ;
- graphe fixe / dynamique.

## Objectifs
- reward partagé ;
- rewards individuels alignés ;
- intérêts mixtes ;
- compétition.

## Population
- taille ;
- renouvellement ;
- remplacement ;
- spécialisation.

---

# Ce qu'il faudra définir proprement

## "Collective"
Est-ce qu'une simple moyenne / vote / ensemble suffit ? Probablement non pour notre question.

## "Cognitive"
Quelles propriétés veut-on qualifier de cognitives ?
- intégration d'information ?
- mémoire ?
- décision ?
- généralisation ?
- représentation ?
- adaptation ?

## "Emergence"
Il faudra éviter :
> "c'est surprenant donc c'est émergent".

Chercher une définition opérationnelle.

## "Similarity"
Pas une étiquette homogène / hétérogène binaire.
Construire éventuellement une métrique multidimensionnelle.

---

# Questions qui doivent rester ouvertes

- Peut-il y avoir cognition collective sans communication explicite ?
- Une population de clones peut-elle produire de la vraie complémentarité ?
- L'hétérogénéité aide-t-elle toujours ?
- Qu'est-ce qui survit quand on remplace un membre par une copie neuve ?
- Qu'est-ce qui survit quand on remplace un agent par un autre modèle ?
- Peut-on avoir synergie sans spécialisation stable ?
- Les LLMs actuels partagent-ils suffisamment de priors culturels pour faciliter une coordination zero-shot inter-familles ?
- Distillation / teacher-student crée-t-elle une forme mesurable de "parenté cognitive" ?
- Peut-on distinguer effet de poids, effet de données et effet de langage partagé ?

---

# Règle

Ajouter ici les nouvelles formulations.

Ne jamais supprimer les anciennes : les dater et expliquer pourquoi elles ont été abandonnées ou raffinées.
