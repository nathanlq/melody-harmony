# Modèles, algorithmes et logiciels pour l'harmonisation de mélodies

**Université de Lille**

**Faculté des Sciences et Technologies**

## Modèles, algorithmes et logiciels pour l’harmonisation de mélodies

### Nathan LECLERCQ

**Master Informatique**  
**Master mention Informatique**

**Département d’Informatique**  
Faculté des Sciences et Technologies  
mai, 2024

Ce mémoire satisfait partiellement les pré-requis du module de Mémoire de Master, pour la 2e année du Master mention Informatique.

**Candidat :** Nathan LECLERCQ, Nº 11700804  
nathan.leclercq.etu@univ-lille.fr

**Encadrant(e) :** Mathieu GIRAUD  
mathieu.giraud@univ-lille.fr

Département d’Informatique  
Faculté des Sciences et Technologies  
Campus Cité Scientifique, Bât. M3 extension, 59655 Villeneuve-d’Ascq  
mai, 2024

## Résumé

Notre recherche vise à dresser un état de l’art récent sur l’harmonisation automatique de mélodies, avec un accent particulier sur les techniques ne nécessitant pas d’entraînement préalable. Comment les méthodes actuelles, notamment celles qui s’affranchissent de l’apprentissage profond et des modèles complexes, parviennent-elles à harmoniser efficacement une mélodie ? Cette question cherche à évaluer les progrès et les tendances du domaine et à en identifier les acteurs.

Pour notre question de recherche, nous allons effectuer une recherche bibliographique. Cela nous permettra de comprendre les avancées récentes dans le domaine de l’harmonisation mélodique, en particulier celles ne nécessitant pas d’apprentissage préalable, et d’identifier les tendances actuelles et futures.

Le protocole est le suivant : on commencera par identifier les sources primaires pour identifier les articles et travaux récents dans le domaine de l’harmonisation mélodique puis dans un second temps on analysera les méthodes ainsi décrites pour enfin les comparer et synthétiser tout cela en mettant l’accent sur les innovations, les améliorations de performance et les limitations.

---

## Chapitre 1 - Fiche nº1

### 1.1 Description de l’article

- **Titre de l’article :** Automatic Melodic Harmonization : An overview, challenges and future directions
- **Lien de l’article :** articles/Automatic Melodic Harmonization.pdf
- **Liste des auteurs :** Dimos Makris, Ioannis Karydis, Spyros Sioutas
- **Affiliation des auteurs :** Department of Informatics, Ionian University, Greece
- **Nom de la conférence / revue :** Trends in Music Information Seeking, Behavior, and Retrieval for Creativity
- **Classification de la conférence / revue :** Ni une conférence, ni une revue (chapitre d’un livre)
- **Nombre de citations de l’article :** 11 (Goggle Scholar), 9 (Semantic scholar), 10 (Igi global)

### 1.2 Synthèse de l’article

- **Problématique :** Il faudrait être capable, à partir d’une ligne mélodique, de générer la suite d’accords correspondante ou tout au moins les suites d’accords les plus probables. L’article explore les fondements et évolutions des différentes méthodes pour réaliser cette tâche.

- **Pistes possibles :** Deux angles d’approche y sont exposés : le premier est de créer un accompagnement harmonique pour une mélodie soprano ; le second de compléter les voix manquantes à partir d’une ligne de basse dans le cadre de l’harmonisation à quatre parties.

- **Question de recherche :** Quelles sont les techniques de référence, leurs fondements et leurs évolutions pour retrouver une harmonisation en partant d’une ligne mélodique soprano ou d’une ligne de basse ?

- **Démarche adoptée :** L’article fait une revue de l’état de l’art de ce domaine en parcourant les différentes approches conceptuelles, soulignant les différences méthodologiques et l’impact des nouvelles représentations de la musique.

- **Implémentation :** Chaque méthode est présentée simplement, parfois avec des schémas, avec des références aux articles et chercheurs clés.

- **Les résultats :** L’harmonisation "four-part harmonization" continue d’évoluer avec de nouvelles idées de modélisation et de prédictions.

---

## Chapitre 2 - Fiche nº2

### 2.1 Description de l’article

- **Titre de l’article :** Algorithmic Harmonization of Tonal Melodies Using Weighted Pitch Context Vectors
- **Lien de l’article :** articles/Weighted Pitch Context Vectors.pdf
- **Liste des auteurs :** Peter Van Kranenburg, Eoin J Kearns
- **Affiliation des auteurs :** Utrecht University, Meertens Institute
- **Nom de la conférence / revue :** International Society for Music Information Retrieval Conference - ISMIR - 2023
- **Classification de la conférence / revue :** A1 sur Conference Ranks
- **Nombre de citations de l’article :** Article récent et encore non cité

### 2.2 Synthèse de l’article

- **Problématique :** Le but est de déduire l’arrière-plan harmonique d’une mélodie à partir de sa notation.

- **Pistes possibles :** L’approche ne nécessite pas d’apprentissage préalable et est basée sur des vecteurs de contexte de hauteur pondérée pour générer des accords candidats.

- **Question de recherche :** Comment déduire l’arrière-plan harmonique d’une mélodie en utilisant des vecteurs de contexte de hauteur pondérée sans apprentissage préalable ?

- **Démarche adoptée :** La démarche consiste à générer des suites d’accords candidates et à choisir la meilleure.

- **Les résultats :** Les résultats évalués par des experts ont montré une harmonisation largement convenable.

---

## Chapitre 3 - Fiche nº3

### 3.1 Description de l’article

- **Titre de l’article :** Melody Harmonization With Interpolated Probabilistic Models
- **Lien de l’article :** articles/Probabilistic Models.pdf
- **Liste des auteurs :** Stanislaw A. Raczynskia, Satoru Fukayamab, Emmanuel Vincent
- **Affiliation des auteurs :** Gdansk University of Technology - Poland, The University of Tokyo - Japan, INRIA - France
- **Nom de la conférence / revue :** Journal of New Music Research - 2012
- **Classification de la conférence / revue :** H-index 40 sur SJR
- **Nombre de citations de l’article :** 37 (Research Gate), 65 (Hal-Inria)

### 3.2 Synthèse de l’article

- **Problématique :** Trouver une suite d’accords à partir d’une mélodie en tenant compte de la tonalité, de la structure rythmique et du style musical.

- **Pistes possibles :** L’article propose une combinaison de plusieurs modèles probabilistes interpolés.

- **Question de recherche :** Comment combiner efficacement plusieurs modèles probabilistes pour harmoniser une mélodie ?

- **Démarche adoptée :** Les sous-modèles sont entraînés sur environ 2000 partitions de chansons populaires.

- **Les résultats :** Le modèle a montré une précision accrue par rapport aux harmonisateurs basés sur des règles.

---

## Chapitre 4 - Fiche nº4

### 4.1 Description de l’article

- **Titre de l’article :** Function- and rhythm-aware melody harmonization based on tree-structured parsing and split-merge sampling of chord sequences
- **Lien de l’article :** articles/Tree Structured Parsing.pdf
- **Liste des auteurs :** Hiroaki Tsushima, Eita Nakamura, Katsutoshi Itoyama, Kazuyoshi Yoshii
- **Affiliation des auteurs :** Graduate School of Informatics, Kyoto University, Japan
- **Nom de la conférence / revue :** International Society for Music Information Retrieval Conference - ISMIR - 2017
- **Classification de la conférence / revue :** A1 sur Conference Ranks
- **Nombre de citations de l’article :** 21 (Semantic Scholar)

### 4.2 Synthèse de l’article

- **Problématique :** Harmoniser en tenant compte de la structure rythmique et des fonctions harmoniques.

- **Pistes possibles :** Utilisation d’une grammaire non contextuelle pour modéliser l’harmonisation en structure d’arbre.

- **Question de recherche :** Comment capturer la structure rythmique et les fonctions harmoniques à l’aide d’une structure hiérarchique ?

- **Démarche adoptée :** Algorithme basé sur "Metropolis-Hastings" pour structurer l’arbre et les symboles d’accords.

- **Les résultats :** Précision bien supérieure par rapport aux HMM.

---

## Chapitre 5 - Fiche nº5

### 5.1 Description de l’article

- **Titre de l’article :** Automatic Melody Harmonization with Triad Chords : A Comparative Study
- **Lien de l’article :** articles/Triad Chords.pdf
- **Liste des auteurs :** Yin-Cheng Yeh, Wen-Yi Hsiao, Satoru Fukayama, Tetsuro Kitahara, Benjamin Genchel, Hao-Min Liu, Hao-Wen Dong, Yian Chen, Terence Leong, Yi-Hsuan Yang
- **Affiliation des auteurs :** Yeh, Hsiao, Liu, Dong, Yang (Academia Sinica - Taiwan), Fukayama (National Institute of Advanced Industrial Science and Technology - Japan), Kitahara (Nihon University - Japan), Genchel (Georgia Institute of Technology - USA), Chen, Leong (KKBOX Inc. - Taiwan)
- **Nom de la conférence / revue :** Journal of New Music Research - 2021
- **Classification de la conférence / revue :** H-index 40 sur SJR
- **Nombre de citations de l’article :** 44 (arXiv, ResearchGate)

### 5.2 Synthèse de l’article

- **Problématique :** Évaluer et comparer différentes méthodes d’harmonisation mélodique automatique.

- **Pistes possibles :** Comparaison de modèles incluant le matching de templates, des modèles HMM, des algorithmes génétiques, et des modèles d’apprentissage profond.

- **Question de recherche :** Quelle méthode est la plus efficace pour harmoniser une mélodie ?

- **Démarche adoptée :** Comparaison rigoureuse de cinq modèles avec des approches différentes.

- **Les résultats :** Les modèles d’apprentissage profond se révèlent plus performants, avec des progressions d’accords plus diversifiées.

---

## Annexe A - Grille d’analyse

Figure A.1 – Analyse comparative des techniques d’harmonisation mélodique.

|                   | Approche                                            | Méthodologie                                                                                                   | Question traitée                                                                  | Entrée                               | Sortie                                | Représentation Musique                                |
| ----------------- | --------------------------------------------------- | -------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------- | ------------------------------------ | ------------------------------------- | ----------------------------------------------------- |
| Makris [2016]     | Etat de l'art                                       | Revue de l'état de l'art présentant les auteurs, les représentations musicales et les technique de prédictions | Présenter les techniques d'harmonisation "four-part"                              | -                                    | -                                     | -                                                     |
| Kranenburg [2023] | Technique d'harmonisation avec vecteurs de contexte | Programmation dynamique                                                                                        | Prédire l'harmonisation d'une mélodie tonale                                      | Mélodie tonale                       | Accords harmonisés                    | Vecteurs de contexte de hauteur                       |
| Tsushima [2017]   | Technique d'harmonisation avec structure d'arbre    | Utilisation d'une modélisation hiérarchique et de grammaire non contextuelle, Algorithme "Metropolis Hasting"  | Prédire une harmonisation en se basant sur les rythmes, les fonctions harmoniques | Mélodie, informations rythmiques     | Séquences d'accords structurées       | Arbre avec structure rythmique, fonctions harmoniques |
| Raczyński [2013]  | Technique d'harmonisation avec modèles interpolés   | Combinaison de modèles probabilistes                                                                           | Prédire une harmonisation en tenant compte des tonalités, et des rythmes          | Mélodie, contexte tonal et rythmique | Séquences d'accords, tonalité ajustée | Séquences représentant tonalité, mélodie              |
| Yeh [2021]        | Comparaison de méthodes d'harmonisation             | Étude comparative des techniques de prédictions des suites d'accords                                           | Comparer les résultats de divers techniques d'harmonisation                       | -                                    | -                                     | -                                                     |
