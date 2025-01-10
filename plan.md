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

#### Transition

L’étude des principes harmoniques et leur modélisation informatique constitue la base sur laquelle reposent les systèmes d’harmonisation automatiques. Ces bases établies, nous pouvons désormais examiner les techniques qui en découlent.

---

## Chapitre 1 : Fondements théoriques de l'harmonisation

### Description du chapitre
Ce chapitre pose les bases théoriques nécessaires pour comprendre l’harmonisation d’un point de vue musical et informatique. Il explore les concepts fondamentaux de l’harmonie musicale ainsi que leur traduction en représentations manipulables par des algorithmes. Il a pour but de donner les clefs de compréhension du domaine en étant le plus accessible et imagé possible (pour les gens interessés).

### 1.1 Concepts musicaux essentiels
- **Contenu :** Définitions des notions fondamentales : accords, tonalité, fonctions harmoniques. Exposition des règles traditionnelles et des différents styles d’harmonisation (à quatre voix, accords simples).
- **Exemple :** Les bases de l'harmonisation traditionnelle dans le style de Bach, exposées dans la fiche 1 (Makris et al.), qui distingue les mélodies soprano des lignes de basse.
- **Progression :** Introduit les concepts musicaux nécessaires à la compréhension des modèles algorithmiques présentés plus tard.

#### Rédaction

L'harmonisation musicale repose sur un ensemble de concepts fondamentaux qui structurent la relation entre mélodie et accompagnement. Au cœur de cette discipline se trouve la notion d'accord, qui représente la superposition simultanée de plusieurs notes créant une sonorité harmonique. Les accords s'organisent autour d'une tonalité, qui établit une hiérarchie entre les différentes notes et définit le contexte harmonique global d'une œuvre.

Dans la tradition occidentale, l'harmonisation à quatre voix, particulièrement développée dans les chorals de Bach, constitue un modèle de référence. Cette approche distribue les notes entre quatre lignes mélodiques : soprano, alto, ténor et basse. La voix supérieure (soprano) porte généralement la mélodie principale, tandis que les autres voix complètent l'harmonie en respectant des règles strictes de progression et d'espacement.

#### Transition :
L’explication des concepts fondamentaux ouvre la voie à la manière dont ces éléments peuvent être représentés et manipulés dans un cadre informatique.

### 1.2 Représentation informatique de la musique
- **Contenu :** Techniques pour encoder la musique : notations MIDI, formats de partitions (MusicXML), structures de données pour manipuler les notes et accords.
- **Exemple :** Description des vecteurs de contexte pondérés pour représenter les notes (fiche 2, Van Kranenburg et Kearns).
- **Transition :** Passage de la théorie musicale à sa modélisation numérique, essentielle pour les approches algorithmiques.

#### Rédaction

La transposition de ces concepts musicaux dans le domaine informatique nécessite des systèmes de représentation adaptés. Le format MIDI, largement utilisé, encode les événements musicaux (notes, durées, vélocités) sous forme de messages numériques. Bien que pratique pour la performance, il ne capture pas toute la richesse de la notation musicale.

Le format MusicXML offre une représentation plus complète, incluant les nuances, les articulations et la structure de la partition. Sa nature XML facilite l'analyse et la manipulation programmatique de la musique.

Les vecteurs de contexte pondérés, introduits par Van Kranenburg et Kearns, représentent une approche novatrice. Ces vecteurs encodent non seulement les hauteurs des notes mais aussi leur importance relative dans le contexte musical, permettant une analyse plus fine des relations harmoniques.

#### Transition

Les représentations les plus riches reposent sur des modélisation adaptés riches et compact, contenant toutes les informations nécessaires pour les algorithmes d'harmonisation. Le choix de la modélisation est essentiel pour l'harmonisation automatique, car il conditionne les techniques algorithmiques utilisées ensuite pour la génération de candidat et impacte donc grandement leurs performances.

Les algorithmes d’harmonisation, qu’ils soient basés sur des règles, des probabilités ou des représentations hiérarchiques, reflètent différentes manières de capturer la richesse et la complexité de la musique. Nous présentons ici ces approches en détaillant leurs forces et limites.

---

## Chapitre 2 : Modélisation et algorithmes pour l’harmonisation automatique

### Description du chapitre
Ce chapitre examine les principales approches algorithmiques utilisées pour générer des harmonisations automatiques. Il présente des méthodes allant des systèmes basés sur des règles jusqu’à des techniques avancées d’optimisation et de représentation hiérarchique.

### 2.1 Approches basées sur les règles
- **Contenu :** Systèmes « rule-based » tels que l’algorithme EMI. Description des limites, comme le manque de flexibilité face aux mélodies complexes.
- **Exemple :** Résultats obtenus par l’algorithme EMI et comparaisons avec des modèles probabilistes (fiche 1).

#### Rédaction

Les premiers systèmes d'harmonisation automatique s'appuyaient sur des règles explicites dérivées de la théorie musicale. L'algorithme EMI (Experiments in Musical Intelligence) représente un exemple emblématique de cette approche. Ces systèmes codifient les règles traditionnelles d'harmonie : évitement des quintes et octaves parallèles, résolution des dissonances, conduite des voix.

#### Transition :
Les limites des systèmes basés sur les règles justifient l’exploration de techniques probabilistes capables de mieux s’adapter aux variations musicales. On peut adopter des modélisation différentes pour mieux représenter d'autres aspects d'une partition.

### 2.2 Approches probabilistes et interpolation
- **Contenu :** Hidden Markov Models (HMM), interpolations de modèles probabilistes pour intégrer les tonalités et rythmes.
- **Exemple :** Modèle probabiliste interpolé de Raczynski et al. (fiche 3), ayant montré des résultats supérieurs aux approches basées sur les règles.
- **Transition :** Introduit les techniques avancées intégrant les probabilités, prélude aux méthodes plus complexes.

#### Rédaction

Les modèles probabilistes, notamment les Modèles de Markov Cachés (HMM), ont introduit une nouvelle perspective dans l'harmonisation automatique. Ces modèles capturent les relations statistiques entre les progressions d'accords, permettant une approche plus nuancée que les systèmes basés sur des règles fixes.

Le travail de Raczynski et al. présente une avancée significative avec l'introduction de modèles probabilistes interpolés. Cette approche combine plusieurs sous-modèles, chacun spécialisé dans un aspect particulier de l'harmonisation : progression harmonique, relation mélodie-harmonie, et structure rythmique.

#### Transition

Les outils mathématiques semblent particulièrement adaptés à la génération d'harmonisation, c'est pourquoi d'autres chercheurs explorent constamment d'autres types de modélisation mathématique et numérique.

### 2.3 Représentations structurées et grammaires
- **Contenu :** Grammaires non contextuelles et parsing d’arbres syntaxiques pour capturer les relations harmoniques hiérarchiques.
- **Exemple :** Algorithme de parsing basé sur Metropolis-Hastings pour structurer les accords en arbres hiérarchiques (fiche 4).

#### Rédaction

L'utilisation de grammaires non contextuelles pour l'harmonisation représente une approche sophistiquée qui capture la nature hiérarchique de la musique. Cette méthode, exemplifiée par les travaux de Tsushima et al., modélise les progressions harmoniques comme des structures arborescentes.

L'algorithme basé sur Metropolis-Hastings permet d'explorer efficacement l'espace des solutions possibles tout en maintenant la cohérence structurelle. Cette approche intègre naturellement les aspects rythmiques et les fonctions harmoniques dans un cadre unifié.

#### Transition

Pour comparer ces approches, il est essentiel de définir des critères d’évaluation objectifs et perceptifs. Cela permettra de mesurer leur pertinence et d’évaluer leurs applications pratiques.

---

## Chapitre 3 : Évaluation des méthodes d’harmonisation

### Description du chapitre
Ce chapitre propose une présentation des techniques d'évaluation des méthodes d’harmonisation en définissant des critères, des protocoles expérimentaux. On fera ensuite une analyse comparative des méthodes présentées plus tôt pour mesurer leur efficacité et leurs limites.

### 3.1 Critères d’évaluation
- **Contenu :** Mesures objectives (précision, rappel), évaluations perceptives (note moyenne d’experts), et respect des règles harmoniques.
- **Exemple :** Exemple de notation de la fiche 2 attribuée par des experts aux harmonisations générées avec les vecteurs de contexte (fiche 2).

#### Rédaction

L'évaluation des systèmes d'harmonisation automatique repose sur plusieurs critères complémentaires. Les mesures objectives incluent la précision (pourcentage d'accords correctement prédits) et le rappel (capacité à identifier toutes les progressions harmoniques pertinentes). Ces métriques sont complétées par des évaluations perceptives réalisées par des experts musicaux.

### Transition :
Pour appliquer ces critères, des méthodologies robustes et des datasets de référence pertinents sont nécessaires.

### 3.2 Méthodologies
- **Contenu :** Protocole expérimental pour tester les algorithmes sur des datasets tels que des mélodies populaires annotées.
- **Exemple :** Comparaison des modèles probabilistes interpolés avec les HMM sur des morceaux annotés (fiche 3).

#### Rédaction

Les protocoles expérimentaux s'appuient sur des datasets de référence, incluant des corpus de musique annotée. Ces collections permettent de comparer objectivement différentes approches sur un même ensemble de mélodies.

La méthodologie développée par Raczynski et al. pour l'évaluation des modèles probabilistes interpolés établit un standard rigoureux. Elle combine validation croisée sur le corpus d'entraînement et tests sur un ensemble de validation indépendant.

### 3.3 Comparaison des approches
- **Contenu :** Analyser les différentes modélisation et évaluation des modèles couverts précédemment par les chercheurs pour les comparer avec des critères similaires. On pourra dégager des avantages et des inconvénients.
- **Exemple :** Les algorithmes génétiques permettent une exploration optimale de l’espace harmonique, comme démontré dans les résultats de la fiche 5.

#### Rédaction

L'analyse comparative révèle les forces et faiblesses de chaque approche. Les systèmes basés sur des règles excellent dans le respect des conventions harmoniques mais manquent de flexibilité. Les modèles probabilistes offrent plus de variété mais peuvent parfois générer des progressions moins conventionnelles.

#### Transition



---

## Chapitre 4 : Implémentations et applications

### Description du chapitre
Ce chapitre explore les outils logiciels et applications pratiques qui mettent en œuvre les concepts étudiés, tout en évaluant leur impact dans des contextes réels tels que l’éducation musicale ou la création artistique.

### 4.1 Outils et frameworks
- **Contenu :** Présentation de logiciels tels que EMI et MTHarmonizer. Analyse comparative de leurs performances et facilité d’utilisation.
- **Exemple :** Certains outils récents intègrent des techniques avancées qui offrent des harmonisations plus variées et adaptées à différents contextes musicaux, tout en restant accessibles aux utilisateurs. Ils illustrent bien la manière dont les concepts théoriques étudiés dans les chapitres précédents peuvent se traduire en applications concrètes.

#### Rédaction

Plusieurs outils logiciels implémentent les concepts théoriques présentés précédemment. EMI et MTHarmonizer représentent deux approches différentes de l'harmonisation automatique. EMI privilégie une approche basée sur des règles strictes, tandis que MTHarmonizer intègre des techniques probabilistes plus flexibles.

#### Transition

Ces outils trouvent des applications concrètes dans divers domaines, allant de l’enseignement à la composition musicale.

### 4.2 Applications pratiques
- **Contenu :** Usages pédagogiques pour l’enseignement musical, outils pour compositeurs, et implications industrielles. Je pourrait ici évoqué notamment le logiciel développé par algomus.
- **Exemple :** Utilisation des harmonisateurs automatiques dans des logiciels éducatifs (fiche 5).
- **Conclusion intermédiaire :** Les implémentations montrent que la théorie peut être transformée en outils fonctionnels.

#### Rédaction

Les applications de l'harmonisation automatique couvrent un large spectre, de l'éducation musicale à la composition assistée par ordinateur. Dans le domaine pédagogique, ces outils offrent aux étudiants la possibilité d'explorer les principes harmoniques de manière interactive.

Le logiciel développé par Algomus illustre particulièrement bien le potentiel de ces applications. Son interface intuitive et ses capacités d'analyse en temps réel en font un outil précieux tant pour l'enseignement que pour la création musicale.

#### Transition

Les implémentations montrent que la théorie peut être transformée en outils fonctionnels. Ces applications concrètes démontrent la viabilité des approches théoriques étudiées et ouvrent la voie à de nouvelles possibilités dans le domaine de l'harmonisation automatique.

---

## Conclusion

- **Synthèse :** Récapitule les méthodes explorées, leurs forces et faiblesses.
- **Tendances :** Croissance des méthodes hybrides combinant règles et apprentissage léger.
- **Perspectives :** Intégration d’algorithmes explicables et interactifs pour améliorer les applications pédagogiques et professionnelles.
- **Recommandations :** Développement de standards pour évaluer l’harmonisation automatique sur des bases musicales diversifiées.

#### Rédaction

Ce mémoire a exploré les avancées récentes dans le domaine de l’harmonisation automatique des mélodies, avec un accent particulier sur les méthodes ne nécessitant pas d’apprentissage profond. Les approches basées sur des règles, bien qu’ancrées dans la tradition musicale, offrent une transparence et une compréhension immédiate des résultats. En revanche, les modèles probabilistes et les grammaires structurées apportent une flexibilité et une richesse d’harmonisation qui répondent mieux à la diversité musicale contemporaine.

Les outils et applications examinés illustrent comment ces méthodes peuvent être mises en pratique pour enrichir la création musicale et l’éducation. Toutefois, plusieurs défis subsistent, notamment l’évaluation standardisée des performances et l’intégration de méthodes interactives et explicables.

L’avenir de l’harmonisation automatique réside probablement dans des approches hybrides qui combinent la rigueur des règles traditionnelles avec la souplesse des modèles probabilistes et l’efficacité de l’apprentissage par faible supervision. Ces systèmes pourraient non seulement améliorer la qualité des harmonisations, mais aussi faciliter l’appropriation par des publics variés, du compositeur à l’étudiant en musique.