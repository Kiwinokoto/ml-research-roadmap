# ROADMAP — Des fondamentaux ML à la recherche en cognition collective artificielle

> **Question directrice provisoire**
>
> **Under what conditions does a population of artificial agents become a collective cognitive system rather than merely a collection of independent agents?**
>
> Cette formulation est volontairement large. L'objectif de la roadmap n'est pas de la figer trop tôt, mais de construire les compétences, les lectures et les expériences nécessaires pour la rendre progressivement plus précise, originale et testable.

## Principe général

Ce parcours est conçu pour quelqu'un qui sait déjà programmer, possède une bonne formation en data science / machine learning, mais veut se remettre à niveau rapidement sur les briques devenues importantes pour ce sujet : reinforcement learning, MARL, game theory, emergent communication, collective intelligence, network science, information theory et systèmes multi-agents à base de LLM.

Le parcours est **orienté fabrication**. À chaque étape théorique correspond une expérience ou un petit projet. Il ne faut pas attendre d'avoir "tout appris" avant de coder.

L'ordre recommandé est :

1. RL fondamental
2. MARL et théorie des jeux
3. premiers environnements multi-agents
4. communication émergente et coordination
5. intelligence collective / systèmes complexes
6. agents cognitifs et LLM multi-agents
7. mesures de cognition collective
8. définition du sujet propre
9. reproduction / expérience originale
10. prise de contact avec les chercheurs

---

# Phase 0 — Installer le cadre de travail

## Objectif

Créer un environnement de recherche personnel où chaque lecture et chaque expérience produit une trace exploitable.

## À faire

- [x] Créer le repo GitHub `ml-research-roadmap`.
- [ ] Mettre `ROADMAP.md` à la racine.
- [ ] Copier les autres fichiers de ce kit sans créer de `README.md` inutile.
- [ ] Utiliser `notes/` pour les fiches de lecture.
- [ ] Utiliser un dossier `experiments/` uniquement quand le premier projet pratique commence.
- [ ] Garder `RESEARCH_QUESTION.md` comme document vivant.
- [ ] Une fois par semaine, noter ce qui a changé dans ta compréhension du sujet.

## Règle

Ne transforme pas le repo en bibliothèque de PDF. Conserve plutôt des **liens vers les versions officielles / arXiv / PMLR / OpenReview**. Cela évite les doublons, les versions obsolètes et les problèmes de licence.

---

# Phase 1 — Réactivation rapide du Reinforcement Learning

## But

Être à l'aise avec la notation et les concepts RL nécessaires pour lire le MARL. Il ne s'agit pas de refaire un cursus complet.

## Concepts à maîtriser

- agent / environment
- state / observation
- action
- reward / return
- policy
- value function / Q-function
- Markov Decision Process (MDP)
- partial observability / POMDP
- exploration vs exploitation
- temporal-difference learning
- Q-learning
- policy gradients
- actor-critic
- on-policy / off-policy

## Ressources principales

### 1. OpenAI — Spinning Up in Deep RL
https://spinningup.openai.com/en/latest/spinningup/rl_intro.html

Lire d'abord l'introduction conceptuelle, sans chercher à maîtriser chaque algorithme.

### 2. Stanford CS234 — Reinforcement Learning, Winter 2026
https://web.stanford.edu/class/cs234/

Parcours minimal conseillé :
- Introduction to RL
- Tabular MDP planning
- Policy evaluation
- Q-learning
- Policy search / policy gradients

### 3. Sutton & Barto — Reinforcement Learning: An Introduction
Référence classique. Stanford renvoie vers la version gratuite depuis CS234.

Pour ce parcours : chapitres 1, 3, 4, 5, 6 et 13 à consulter de manière ciblée, pas forcément linéaire.

### 4. David Silver — Reinforcement Learning Course
Cours DeepMind historique mais toujours excellent pour l'intuition :
https://www.youtube.com/watch?v=2pWv7GOvuf0

## Mini-projet 1 — RL from scratch

Implémenter sans grosse librairie :
- un bandit multi-bras ;
- puis un petit GridWorld avec Q-learning.

### Critère de sortie

Tu dois pouvoir expliquer sans notes :
- pourquoi un reward immédiat n'est pas le return ;
- différence entre policy et value function ;
- différence entre Q-learning et policy gradient ;
- ce qu'est un MDP ;
- pourquoi partial observability change le problème.

---

# Phase 2 — Fondamentaux MARL

## Ressource centrale

### Multi-Agent Reinforcement Learning: Foundations and Modern Approaches
Stefano V. Albrecht, Filippos Christianos, Lukas Schäfer — MIT Press, 2024.

Site officiel :
https://www.marl-book.com/

PDF gratuit officiel :
https://www.marl-book.com/download/marl-book.pdf

Le site contient également code, exercices et slides.

## Ordre de lecture conseillé

### Premier passage
- chapitre 1 — Introduction
- chapitre 2 — Reinforcement Learning
- chapitre 3 — Games: Models of Multi-Agent Interaction
- chapitre 4 — Solution Concepts for Games
- chapitre 5 — First Steps and Challenges

### Deuxième passage
- chapitre 6 — Foundational Algorithms
- chapitre 9 — Multi-Agent Deep Reinforcement Learning
- chapitre 10 — MARL in Practice
- chapitre 11 — Multi-Agent Environments

### Chapitres 7–8
Utiliser comme remise à niveau Deep Learning / Deep RL si besoin. Ne pas les lire intégralement par principe si les concepts sont déjà acquis.

## Concepts MARL indispensables

- Markov games / stochastic games
- cooperative vs competitive vs mixed settings
- Nash equilibrium
- self-play
- non-stationarity
- equilibrium selection
- multi-agent credit assignment
- decentralized execution
- CTDE — Centralized Training, Decentralized Execution
- parameter sharing
- opponent / partner modelling
- zero-shot coordination
- social generalization

## Mini-projet 2 — PettingZoo

PettingZoo :
https://pettingzoo.farama.org/

Commencer par un environnement simple :
- Rock-Paper-Scissors ;
- simple coordination game ;
- éventuellement Cooperative Pong ensuite.

Faire varier :
- même policy pour plusieurs agents ;
- policies séparées ;
- reward partagé ou individuel ;
- observation complète ou partielle.

### Critère de sortie

Tu dois pouvoir expliquer :
- pourquoi MARL n'est pas seulement "plusieurs RL en parallèle" ;
- le problème de non-stationarity ;
- ce que CTDE résout et ce qu'il ne résout pas ;
- ce que signifie parameter sharing ;
- pourquoi self-play peut apprendre des conventions fragiles.

---

# Phase 3 — Communication émergente et conventions

Cette phase rejoint directement ton ancien projet d'agents évolutifs capables de créer un moyen de communication avec un coût.

## Lectures

### Foerster et al. — Learning to Communicate with Deep Multi-Agent Reinforcement Learning (2016)
https://papers.nips.cc/paper/6042-learning-to-communicate-with-deep-multi-agent-reinforcement-learning

Questions :
- quelle information doit être transmise ?
- pourquoi la communication devient-elle utile ?
- différence RIAL / DIAL ;
- que permet l'apprentissage centralisé ?

### Lowe et al. — On the Pitfalls of Measuring Emergent Communication (2019)
https://arxiv.org/abs/1903.05168

Lecture très importante.

Question centrale : un signal corrélé avec une action est-il réellement **causalement utilisé** par l'autre agent ?

### Hu et al. — Other-Play for Zero-Shot Coordination (2020)
https://arxiv.org/abs/2003.02979

Question :
- pourquoi des agents excellents en self-play peuvent-ils échouer avec un partenaire nouveau ?

### Treutlein et al. — A New Formalism, Method and Open Issues for Zero-Shot Coordination (2021)
https://arxiv.org/abs/2106.06613

À lire après Other-Play, pas avant.

## Mini-projet 3 — Costly Communication

Reprendre l'idée de ton ancien projet.

### Monde minimal

Deux ou plusieurs agents doivent coopérer dans un environnement partiellement observable.

Ils peuvent émettre un symbole parmi un petit vocabulaire.

Chaque message a un coût :
\[
r_{total} = r_{task} - \lambda \times communication\_cost
\]

Faire varier progressivement \(\lambda\).

### Expériences

- canal gratuit ;
- canal légèrement coûteux ;
- canal très coûteux ;
- bande passante limitée ;
- bruit dans le canal ;
- suppression complète du canal après apprentissage ;
- partenaire remplacé par un agent jamais rencontré.

### Mesures

Ne pas regarder uniquement le reward :
- fréquence de communication ;
- entropie des symboles ;
- information mutuelle message / état ;
- ablation du canal ;
- permutation aléatoire des messages ;
- performance avec partenaire nouveau.

### Question intéressante

Existe-t-il une zone de coût où la communication devient **rare mais hautement informative** ?

---

# Phase 4 — Autocurricula, innovation et open-ended learning

## Lecture déclencheuse

### OpenAI — Emergent Tool Use from Multi-Agent Interaction / Hide-and-Seek (2019)
https://openai.com/index/emergent-tool-use/

Revenir au papier / article qui a déclenché ton intuition initiale.

Questions :
- comment une stratégie crée-t-elle la pression sélective qui fait apparaître la suivante ?
- quel rôle joue le reward collectif ?
- qu'est-ce qui relève de l'agent individuel et qu'est-ce qui existe seulement par co-adaptation ?

## FLOWERS / Moulin-Frier

### Nisioti et al. — Social Network Structure Shapes Innovation: Experience-sharing in RL with SAPIENS
https://arxiv.org/abs/2206.05060

### Nisioti et al. — Autotelic Reinforcement Learning in Multi-Agent Environments
https://proceedings.mlr.press/v232/nisioti23a.html

Questions :
- pourquoi la topologie des interactions modifie-t-elle l'innovation ?
- comment apparaissent alignement des objectifs et spécialisation ?
- qu'est-ce qu'un agent autotelic ?
- comment mesurer autre chose que le reward ?

## Mini-projet 4 — La topologie compte-t-elle ?

Créer une population d'agents identiques qui partagent seulement une partie de leur expérience.

Comparer :
- réseau totalement connecté ;
- anneau ;
- petits mondes ;
- réseau dynamique ;
- groupes temporaires.

Mesurer :
- diversité des expériences ;
- vitesse de convergence ;
- innovation / découverte ;
- homogénéisation prématurée ;
- spécialisation.

Ce projet prépare directement à la question : **un collectif peut-il perdre en intelligence parce qu'il communique trop bien ?**

---

# Phase 5 — Collective intelligence et systèmes complexes

Ici, on sort volontairement de la seule tradition MARL.

## Ressource de fond

### Barabási — Network Science
Livre en ligne gratuit :
https://networksciencebook.com/

Ne pas tout lire. Priorité :
- network measures ;
- random networks ;
- small-world effects ;
- community structure ;
- diffusion / spreading phenomena.

## Pôle Vito Trianni / CINARS

Profil :
https://istc.cnr.it/en/people/vito-trianni

CINARS — Collective Intelligence in Natural and Artificial Systems:
https://istc.cnr.it/en/group/cinars

But de cette lecture :
- comprendre la tradition swarm intelligence / distributed cognition ;
- identifier ce que les chercheurs LLM redécouvrent éventuellement sous un nouveau vocabulaire ;
- voir comment une propriété cognitive peut être définie au niveau du système plutôt qu'au niveau des composants.

## Mini-projet 5 — Même intelligence locale, topologies différentes

Donner exactement la même policy / architecture à tous les agents.

Faire varier uniquement :
- nombre d'agents ;
- graphe d'interaction ;
- rayon d'observation ;
- fréquence des interactions.

Chercher :
- transitions de régime ;
- consensus ;
- fragmentation ;
- spécialisation ;
- effets de seuil.

---

# Phase 6 — LLMs, agents cognitifs et émergence d'un niveau collectif

À ce stade seulement, passer sérieusement aux systèmes multi-agents basés sur LLM.

## Lecture centrale

### Christoph Riedl — Emergent Coordination in Multi-Agent Language Models
ICLR 2026.
https://riedlc.github.io/Emergent-Coordination-in-Multi-Agent-Language-Models/

arXiv :
https://arxiv.org/abs/2510.05174

Objectif : lire le papier entièrement.

Créer une fiche spéciale répondant à :
1. Quelle définition opérationnelle de l'émergence ?
2. Quelle métrique ?
3. Quels agents ?
4. Quelle communication ?
5. Quelles interventions causales ?
6. Quels résultats sont réellement démontrés ?
7. Quelles variables ne sont pas testées ?
8. Quel résultat pourrait falsifier l'interprétation proposée ?

### Zomer & De Domenico — Unraveling the emergence of collective behavior in networks of cognitive agents
npj Artificial Intelligence, 2026.
https://www.nature.com/articles/s44387-026-00091-5

Observer notamment :
- effet de la topologie ;
- interaction entre intelligence individuelle et comportement collectif ;
- consensus et phénomènes émergents.

## Mini-projet 6 — Reproduction minimale de Riedl

Ne pas commencer par une réplication complète.

Construire un jeu collectif simple avec 3–5 agents LLM.

Comparer :
- agents indépendants ;
- personas ;
- instruction de modéliser ce que les autres agents vont faire ;
- communication directe ;
- pas de communication ;
- feedback global.

Mesurer d'abord des choses simples :
- performance ;
- diversité des réponses ;
- stabilité des rôles ;
- complémentarité.

Puis seulement introduire les métriques informationnelles avancées.

---

# Phase 7 — Axe original : la similarité entre agents comme variable causale

À ce stade, ne plus utiliser "homogeneous" comme une frontière de périmètre.

Utiliser **agent similarity / relatedness** comme variable expérimentale.

## Question candidate

> **What causal role does agent similarity play in the emergence of collective cognition?**

Sous-question possible :

> **How do shared priors, representations and training histories shape the emergence of collective cognition in populations of artificial agents?**

## Construire une échelle de similarité

Exemple :

1. même modèle, mêmes poids, même prompt ;
2. même modèle, mêmes poids, prompts / rôles différents ;
3. même checkpoint, historiques de mémoire différents ;
4. mêmes poids initiaux, fine-tunes différents ;
5. même famille de modèles, checkpoints différents ;
6. modèles issus de distillation / teacher-student ;
7. architectures ou fournisseurs différents mais langage / données culturelles largement partagés ;
8. agents fortement hétérogènes.

Attention : cette échelle n'est pas encore une métrique scientifique. Elle sert à générer des hypothèses.

## Mini-projet 7 — Similarity Sweep

Choisir une tâche collective stable.

Faire varier uniquement la relation entre agents.

Questions :
- la similarité augmente-t-elle la coordination zero-shot ?
- trop de similarité détruit-elle la complémentarité ?
- existe-t-il un optimum entre alignement et diversité ?
- quelles propriétés sont dues aux priors partagés ?
- lesquelles nécessitent une histoire commune ?
- quelles propriétés survivent au remplacement d'un membre ?

Ce projet est un candidat sérieux pour devenir une première expérience de recherche.

---

# Phase 8 — Information theory et mesure de la cognition collective

Cette phase peut demander une remise à niveau mathématique ciblée.

## Concepts

- entropy
- conditional entropy
- mutual information
- KL divergence
- total correlation
- redundancy
- synergy
- Partial Information Decomposition (PID)
- time-delayed mutual information
- causal interventions / ablations

Ne pas apprendre toute la théorie de l'information avant d'en avoir besoin.

Commencer par comprendre :
\[
I(X;Y)
\]
et pourquoi corrélation / information ne suffisent pas à établir une causalité.

## Projet

Reprendre un de tes environnements précédents et tenter de distinguer :

- information redondante ;
- information unique ;
- information synergique.

Question fondamentale :

> Une information utile à la réussite existe-t-elle uniquement dans la combinaison de plusieurs agents, et non dans aucun agent considéré séparément ?

C'est beaucoup plus fort que :
> "le groupe obtient un meilleur score".

---

# Phase 9 — Définir le vrai sujet

Cette phase commence en réalité dès le jour 1 dans `RESEARCH_QUESTION.md`, mais ici elle devient formelle.

## Livrables

### 1. État de l'art court
10–20 pages maximum.

### 2. Matrice de littérature
Pour chaque papier :
- question ;
- agents ;
- environnement ;
- apprentissage ;
- interaction ;
- degré de similarité ;
- communication ;
- métriques ;
- interventions ;
- résultat ;
- limitation ;
- expérience suivante souhaitée.

### 3. Une page "Research gap"
Pas de grande déclaration philosophique.

Écrire :
- ce qui est déjà bien établi ;
- ce qui est encore mal mesuré ;
- quelle variable manque ;
- quelle expérience permettrait de trancher.

### 4. Trois questions candidates
Les rendre falsifiables.

### 5. Une expérience pilote
Idéalement déjà exécutée, même petite.

---

# Phase 10 — Quand commencer à contacter les chercheurs ?

**Pas besoin d'attendre d'être "expert".**

Le premier contact devient raisonnable dès que les cinq conditions suivantes sont remplies :

- [ ] tu comprends RL + MARL sans buter sur le vocabulaire fondamental ;
- [ ] tu as lu attentivement environ 6–10 papiers centraux ;
- [ ] tu as réalisé au moins deux petites expériences multi-agents ;
- [ ] tu as une note d'une page décrivant ta question et ce qui te semble encore ouvert ;
- [ ] tu peux citer précisément 1–2 travaux de la personne contactée et expliquer pourquoi ton questionnement s'y rattache.

À ce moment-là, **contact exploratoire**, pas demande solennelle de direction de thèse immédiatement.

## Ordre possible

### Pôle 1 — FLOWERS / BioTiC
**Pierre-Yves Oudeyer — FLOWERS, Bordeaux**
https://flowers.inria.fr/team/

**Clément Moulin-Frier — BioTiC, Inria Lyon**
État actuel de l'équipe :
https://radar.inria.fr/report/2025/biotic/index.html

À contacter lorsque tu as lu au minimum :
- SAPIENS ;
- Autotelic RL in Multi-Agent Environments ;
- un ou deux travaux récents sur évolution culturelle / agents autotelic.

Pourquoi : meilleur alignement avec émergence, open-endedness, cognition, culture et multi-agent learning.

### Pôle 2 — Christoph Riedl — Northeastern
Projet :
https://riedlc.github.io/Emergent-Coordination-in-Multi-Agent-Language-Models/

Programme actuel :
https://www.christophriedl.net/jobs.html

À contacter après lecture très sérieuse de son papier ICLR 2026 et idéalement une reproduction / extension minimale.

Pourquoi : il attaque directement la frontière "collection d'agents vs collectif intégré".

### Pôle 3 — Jakob Foerster — Oxford
https://eng.ox.ac.uk/people/jakob-foerster

À contacter une fois que tu maîtrises :
- emergent communication ;
- zero-shot coordination ;
- self-play / partner generalization.

Pourquoi : fondations du deep MARL, communication et coordination entre partenaires inconnus.

### Pôle 4 — Vito Trianni — CNR / CINARS, Rome
https://istc.cnr.it/en/people/vito-trianni
https://istc.cnr.it/en/group/cinars

À contacter une fois que tu peux relier ton problème aux notions de :
- distributed cognition ;
- self-organization ;
- network topology ;
- swarm / collective intelligence.

Pourquoi : apporte la profondeur systèmes complexes / cognition distribuée qui peut empêcher de réduire le sujet à "plusieurs LLM qui parlent".

## Important

Ne contacte pas les quatre pôles avec le même mail générique.

Chaque premier message devra expliquer :
- ce que tu as lu chez eux ;
- le point précis qui t'intéresse ;
- ta question actuelle ;
- l'expérience que tu envisages ;
- ce que tu souhaites : échange court, avis sur l'angle, possibilités de thèse, etc.

---

# Phase 11 — Projet-capstone avant une proposition de thèse

## Nom provisoire
**Collective Cognition Sandbox**

Construire un environnement expérimental où plusieurs dimensions sont contrôlables :

### Agent
- architecture ;
- paramètres ;
- historique ;
- rôle ;
- mémoire.

### Interaction
- graphe ;
- fréquence ;
- canal ;
- coût ;
- bruit ;
- bande passante.

### Objectif
- individuel ;
- partagé ;
- partiellement aligné.

### Population
- taille ;
- homogénéité / diversité ;
- remplacement de membres ;
- agents inconnus.

### Mesures
- reward collectif ;
- robustesse ;
- zero-shot coordination ;
- spécialisation ;
- diversité ;
- ablations ;
- information unique / redondante / synergique.

Ce sandbox ne doit pas naître gros. Commencer par un environnement minuscule où chaque hypothèse est testable.

---

# Définition de réussite de cette roadmap

Cette roadmap est terminée lorsque tu peux :

1. lire un papier MARL contemporain sans blocage conceptuel majeur ;
2. implémenter et modifier un environnement multi-agent ;
3. distinguer performance, coordination, communication et cognition collective ;
4. expliquer les principales traditions : MARL, emergent communication, open-ended learning, collective intelligence, complex systems ;
5. reproduire au moins un résultat publié à petite échelle ;
6. proposer une expérience dont le résultat pourrait réfuter ton hypothèse ;
7. formuler une question de thèse assez précise pour être testée mais assez large pour produire plusieurs contributions ;
8. écrire à 2–4 chercheurs avec une proposition intellectuellement crédible.

La roadmap n'est donc pas "finir une liste de cours". Son objectif final est : **devenir capable de formuler, tester et défendre ton propre problème de recherche.**
