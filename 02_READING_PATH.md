# 02 — Reading Path

Ordre conseillé. Le but n'est pas de tout lire avant de coder.

## Niveau 0 — références / remise à niveau

### MARL textbook — Albrecht, Christianos, Schäfer (2024)
https://www.marl-book.com/

**Pourquoi :** référence structurante couvrant RL, game theory, MARL et deep MARL.

### Stanford CS234 (2026)
https://web.stanford.edu/class/cs234/

**Pourquoi :** remise à niveau RL moderne structurée.

### OpenAI Spinning Up
https://spinningup.openai.com/en/latest/spinningup/rl_intro.html

**Pourquoi :** réactivation rapide du vocabulaire RL.

---

## Niveau 1 — naissance du problème moderne de communication multi-agent

### Foerster et al. (2016)
**Learning to Communicate with Deep Multi-Agent Reinforcement Learning**
https://papers.nips.cc/paper/6042-learning-to-communicate-with-deep-multi-agent-reinforcement-learning

Questions :
- pourquoi les agents ont-ils besoin d'un protocole ?
- quelle différence entre communication discrète et différentiable ?
- quel est le rôle du centralized training ?

### Lowe et al. (2019)
**On the Pitfalls of Measuring Emergent Communication**
https://arxiv.org/abs/1903.05168

Questions :
- comment distinguer corrélation et communication causale ?
- quelles ablations sont indispensables ?

### OpenAI (2019)
**Emergent Tool Use from Multi-Agent Interaction**
https://openai.com/index/emergent-tool-use/

Questions :
- qu'est-ce qu'un autocurriculum ?
- comment des stratégies nouvelles créent-elles leurs propres pressions d'apprentissage ?

---

## Niveau 2 — coordination avec des partenaires nouveaux

### Hu et al. (2020)
**Other-Play for Zero-Shot Coordination**
https://arxiv.org/abs/2003.02979

### Treutlein et al. (2021)
**A New Formalism, Method and Open Issues for Zero-Shot Coordination**
https://arxiv.org/abs/2106.06613

### DeepMind (2021)
**Melting Pot: an evaluation suite for multi-agent reinforcement learning**
https://deepmind.google/blog/melting-pot-an-evaluation-suite-for-multi-agent-reinforcement-learning/

Questions :
- qu'est-ce qu'une convention ?
- comment tester la social generalization ?
- quelle part de coordination vient d'une histoire partagée ?

---

## Niveau 3 — FLOWERS / innovation / autotelic agents

### Nisioti et al. (2022)
**Social Network Structure Shapes Innovation: Experience-sharing in RL with SAPIENS**
https://arxiv.org/abs/2206.05060

### Nisioti et al. (2023)
**Autotelic Reinforcement Learning in Multi-Agent Environments**
https://proceedings.mlr.press/v232/nisioti23a.html

Questions :
- rôle de la topologie sociale ;
- diversité vs convergence ;
- goal alignment ;
- specialization ;
- émergence décentralisée.

---

## Niveau 4 — systèmes complexes / intelligence collective

### Barabási — Network Science
https://networksciencebook.com/

### Vito Trianni / CINARS
https://istc.cnr.it/en/people/vito-trianni
https://istc.cnr.it/en/group/cinars

Objectif :
- apprendre le vocabulaire de self-organization, swarm intelligence et distributed cognition ;
- comparer cette tradition aux systèmes multi-LLM modernes.

---

## Niveau 5 — cognition collective chez les LLMs

### Christoph Riedl (ICLR 2026)
**Emergent Coordination in Multi-Agent Language Models**
https://riedlc.github.io/Emergent-Coordination-in-Multi-Agent-Language-Models/
https://arxiv.org/abs/2510.05174

Lecture approfondie obligatoire avant prise de contact.

### Zomer & De Domenico (2026)
**Unraveling the emergence of collective behavior in networks of cognitive agents**
https://www.nature.com/articles/s44387-026-00091-5

Questions :
- comment définit-on un changement de régime collectif ?
- comment la topologie interagit-elle avec la capacité cognitive individuelle ?
- quel rôle joue le consensus ?

---

## Ordre de lecture résumé

1. MARL book ch. 1–5
2. Foerster 2016
3. Lowe 2019
4. OpenAI Hide-and-Seek 2019
5. Other-Play 2020
6. Melting Pot 2021
7. SAPIENS 2022
8. Autotelic MARL 2023
9. Network Science — lectures ciblées
10. Riedl 2026
11. Zomer & De Domenico 2026
12. revenir au MARL book ch. 6, 9–11 selon les besoins

## Règle de lecture

Pour chaque papier, utiliser `templates/PAPER_NOTE.md`.

Ne faire un résumé exhaustif que si le papier devient central.

Sinon, chercher surtout :
- ce qu'il mesure ;
- ce qu'il manipule ;
- ce qu'il ne teste pas ;
- quelle expérience suivante tu voudrais faire.
