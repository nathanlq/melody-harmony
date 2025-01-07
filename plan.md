## Résumé

Notre recherche vise à dresser un état de l'art récent sur l'harmonisation automatique de mélodies, avec un accent particulier sur les techniques ne nécessitant pas d'entraînement préalable. Comment les méthodes actuelles, notamment celles qui s'affranchissent de l'apprentissage profond et des modèles complexes, parviennent-elles à harmoniser efficacement une mélodie ? Cette question cherche à évaluer les progrès et les tendances du domaine et à en identifier les acteurs.

Pour notre question de recherche, nous allons effectuer une recherche bibliographique. Cela nous permettra de comprendre les avancées récentes dans le domaine de l'harmonisation mélodique, en particulier celles ne nécessitant pas d'apprentissage préalable, et d'identifier les tendances actuelles et futures.

Le protocole est le suivant : on commencera par identifier les sources primaires pour identifier les articles et travaux récents dans le domaine de l'harmonisation mélodique puis dans un second temps on analysera les méthodes ainsi décrites pour enfin les comparer et synthétiser tout cela en mettant l'accent sur les innovations, les améliorations de performance et les limitations.

## Table des matières

1. Introduction
2. Fondements théoriques de l'harmonisation
   2.1. Concepts musicaux essentiels
   2.2. Représentation informatique de la musique
3. Modélisation et algorithmes pour l’harmonisation automatique
   3.1. Approches basées sur les règles
   3.2. Approches probabilistes et interpolation
   3.3. Représentations structurées et grammaires
4. Évaluation des méthodes d’harmonisation
   4.1. Critères d'évaluation
   4.2. Méthodologies
   4.3. Comparaison des approches
5. Implémentations et applications
   5.1. Outils et frameworks
   5.2. Applications pratiques
6. Conclusion

## Introduction

### Contexte
L'harmonisation automatique de mélodies est un défi complexe en informatique musicale. Elle combine les connaissances musicales et des approches algorithmiques pour créer des harmonisations qui respectent les règles musicales tout en proposant des solutions innovantes.

Les théoriciens de la musique ont établi depuis longtemps des règles d'harmonisation traditionnelles, comme celles utilisées dans le style de Bach. Ces règles servent de base aux approches algorithmiques modernes qui tentent d'automatiser le processus d'harmonisation. Cependant, avec l'émergence de l'intelligence artificielle, de nouvelles méthodes basées sur l'apprentissage profond ont gagné en popularité, laissant parfois dans l'ombre des approches plus traditionnelles. Cependant, certaines présentent pourtant des avantages significatifs, notamment en termes de transparence et d'absence de nécessité d'entraînement préalable.

### Problématique
Comment les méthodes actuelles, notamment celles ne nécessitant pas d'apprentissage profond, parviennent-elles à harmoniser efficacement une mélodie ? Quels sont les avantages et limites de ces approches ?

Cette recherche vise à dresser un état de l'art actualisé des méthodes d'harmonisation, en mettant l'accent sur les approches qui ne reposent pas sur l'apprentissage profond. Notre analyse s'appuie sur une revue approfondie de la littérature scientifique récente, particulièrement des publications issues de la conférence ISMIR, référence dans le domaine de la recherche en informatique musicale.

### Justification du plan
Le plan suit une progression logique allant des bases conceptuelles et théoriques aux méthodes pratiques et leur évaluation. Cette structure favorise une compréhension approfondie des enjeux, des méthodes, et des applications dans le domaine.

Ce mémoire s'organise en commençant par les fondements théoriques nécessaires à la compréhension de l'harmonisation musicale, avant d'explorer les différentes approches algorithmiques. Nous examinerons ensuite les méthodes d'évaluation de ces systèmes, pour finir par leurs applications pratiques et leurs implémentations concrètes. Cette progression permettra de comprendre l'état actuel de la recherche et d'identifier les perspectives futures dans ce domaine en constante évolution.

---

## Chapitre 1 : Fondements théoriques de l'harmonisation

### Description du chapitre
Ce chapitre pose les bases théoriques nécessaires pour comprendre l’harmonisation d’un point de vue musical et informatique. Il explore les concepts fondamentaux de l’harmonie musicale ainsi que leur traduction en représentations manipulables par des algorithmes. Il a pour but de donner les clefs de compréhension du domaine en étant le plus accessible et imagé possible (pour les gens interessés).

### 1.1 Concepts musicaux essentiels
- **Contenu :** Définitions des notions fondamentales : accords, tonalité, fonctions harmoniques. Exposition des règles traditionnelles et des différents styles d’harmonisation (à quatre voix, accords simples).
- **Exemple :** Les bases de l'harmonisation traditionnelle dans le style de Bach, exposées dans la fiche 1 (Makris et al.), qui distingue les mélodies soprano des lignes de basse.
- **Progression :** Introduit les concepts musicaux nécessaires à la compréhension des modèles algorithmiques présentés plus tard.

### Transition :
L’explication des concepts fondamentaux ouvre la voie à la manière dont ces éléments peuvent être représentés et manipulés dans un cadre informatique.

### 1.2 Représentation informatique de la musique
- **Contenu :** Techniques pour encoder la musique : notations MIDI, formats de partitions (MusicXML), structures de données pour manipuler les notes et accords.
- **Exemple :** Description des vecteurs de contexte pondérés pour représenter les notes (fiche 2, Van Kranenburg et Kearns).
- **Transition :** Passage de la théorie musicale à sa modélisation numérique, essentielle pour les approches algorithmiques.

---

## Chapitre 2 : Modélisation et algorithmes pour l’harmonisation automatique

### Description du chapitre
Ce chapitre examine les principales approches algorithmiques utilisées pour générer des harmonisations automatiques. Il présente des méthodes allant des systèmes basés sur des règles jusqu’à des techniques avancées d’optimisation et de représentation hiérarchique.

### 2.1 Approches basées sur les règles
- **Contenu :** Systèmes « rule-based » tels que l’algorithme EMI. Description des limites, comme le manque de flexibilité face aux mélodies complexes.
- **Exemple :** Résultats obtenus par l’algorithme EMI et comparaisons avec des modèles probabilistes (fiche 1).

### Transition :
Les limites des systèmes basés sur les règles justifient l’exploration de techniques probabilistes capables de mieux s’adapter aux variations musicales. On peut adopter des modélisation différentes pour mieux représenter d'autres aspects d'une partition.

### 2.2 Approches probabilistes et interpolation
- **Contenu :** Hidden Markov Models (HMM), interpolations de modèles probabilistes pour intégrer les tonalités et rythmes.
- **Exemple :** Modèle probabiliste interpolé de Raczynski et al. (fiche 3), ayant montré des résultats supérieurs aux approches basées sur les règles.
- **Transition :** Introduit les techniques avancées intégrant les probabilités, prélude aux méthodes plus complexes.

### 2.3 Représentations structurées et grammaires
- **Contenu :** Grammaires non contextuelles et parsing d’arbres syntaxiques pour capturer les relations harmoniques hiérarchiques.
- **Exemple :** Algorithme de parsing basé sur Metropolis-Hastings pour structurer les accords en arbres hiérarchiques (fiche 4).

---

## Chapitre 3 : Évaluation des méthodes d’harmonisation

### Description du chapitre
Ce chapitre propose une présentation des techniques d'évaluation des méthodes d’harmonisation en définissant des critères, des protocoles expérimentaux. On fera ensuite une analyse comparative des méthodes présentées plus tôt pour mesurer leur efficacité et leurs limites.

### 3.1 Critères d’évaluation
- **Contenu :** Mesures objectives (précision, rappel), évaluations perceptives (note moyenne d’experts), et respect des règles harmoniques.
- **Exemple :** Exemple de notation de la fiche 2 attribuée par des experts aux harmonisations générées avec les vecteurs de contexte (fiche 2).

### Transition :
Pour appliquer ces critères, des méthodologies robustes et des datasets de référence pertinents sont nécessaires.

### 3.2 Méthodologies
- **Contenu :** Protocole expérimental pour tester les algorithmes sur des datasets tels que des mélodies populaires annotées.
- **Exemple :** Comparaison des modèles probabilistes interpolés avec les HMM sur des morceaux annotés (fiche 3).

### 3.3 Comparaison des approches
- **Contenu :** Analyser les différentes modélisation et évaluation des modèles couverts précédemment par les chercheurs pour les comparer avec des critères similaires. On pourra dégager des avantages et des inconvénients.
- **Exemple :** Les algorithmes génétiques permettent une exploration optimale de l’espace harmonique, comme démontré dans les résultats de la fiche 5.

---

## Chapitre 4 : Implémentations et applications

### Description du chapitre
Ce chapitre explore les outils logiciels et applications pratiques qui mettent en œuvre les concepts étudiés, tout en évaluant leur impact dans des contextes réels tels que l’éducation musicale ou la création artistique.

### 4.1 Outils et frameworks
- **Contenu :** Présentation de logiciels tels que EMI et MTHarmonizer. Analyse comparative de leurs performances et facilité d’utilisation.
- **Exemple :** Certains outils récents intègrent des techniques avancées qui offrent des harmonisations plus variées et adaptées à différents contextes musicaux, tout en restant accessibles aux utilisateurs. Ils illustrent bien la manière dont les concepts théoriques étudiés dans les chapitres précédents peuvent se traduire en applications concrètes.

### Transition :
Ces outils trouvent des applications concrètes dans divers domaines, allant de l’enseignement à la composition musicale.

### 4.2 Applications pratiques
- **Contenu :** Usages pédagogiques pour l’enseignement musical, outils pour compositeurs, et implications industrielles. Je pourrait ici évoqué notamment le logiciel développé par algomus.
- **Exemple :** Utilisation des harmonisateurs automatiques dans des logiciels éducatifs (fiche 5).
- **Conclusion intermédiaire :** Les implémentations montrent que la théorie peut être transformée en outils fonctionnels.

---

## Conclusion

- **Synthèse :** Récapitule les méthodes explorées, leurs forces et faiblesses.
- **Tendances :** Croissance des méthodes hybrides combinant règles et apprentissage léger.
- **Perspectives :** Intégration d’algorithmes explicables et interactifs pour améliorer les applications pédagogiques et professionnelles.
- **Recommandations :** Développement de standards pour évaluer l’harmonisation automatique sur des bases musicales diversifiées.
