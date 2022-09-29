# Statistique (en 120 minutes :clock2:)

## Préambule

L'objectif, certes ambitieux, de ce document est de rassembler les outils statistiques
classiques pour mener à bien l'analyse de données expérimentales.

## 1. Terminologie

La statistique est un **chaînon important de la démarche scientifique**. En effet, afin de
valider une hypothèse théorique, les scientifiques formulent une question de recherche
qui sera testée à l'aide d'un protocole expérimental. Les outils statistiques permettent
d'analyser les données mesurées lors de l'expérimentation afin d'apporter des éléments de
réponse **objectifs** à la question initiale.

***population*** : l'ensemble des individus concernés par la question de recherche

***échantillon*** : sous-ensemble de la population participant à l'expérience

> Afin de pouvoir généraliser les résultats obtenus sur l'échantillon à
> l'ensemble de la population, celui-ci doit être **représentatif**.
> La méthode idéale pour constituer
> un échantillon consiste en un **tirage aléatoire** afin d'éviter tout biais.

***variable*** : une caractéristique étudiée par la question de recherche (sexe, âge,
taille, ville de naissance, ...)

> Les variables peuvent être de deux natures : 
> - quantitatives : représentées par une valeur numérique (âge, taille)
> - qualitatives : représentées par un attribut ou une classe (sexe, ville de naissance) 

Ce document, pour des raisons de temps, ne traite que des statistiques des variables quantitatives.

***jeu de données*** : un ensemble de variables mesurées pour chaque individu de 
l'échantillon. Celui-ci se présente sous la forme d'un tableau, les colonnes
représentant les variables et les lignes les individus composant l'échantillon.

Le fichier [L1-STAPS.xlsx](data/L1-STAPS.xlsx) servira de fil rouge pour illustrer
les différents outils statistiques abordés dans ce document. Il représente un
échantillon de 31 étudiants de Licence 1 STAPS avec les variables suivantes :
- Sexe
- Âge
- Pulsations cardiaques $P_0$, $P_1$ et $P_2$
- indices à l'issue des tests de [Ruffier](https://fr.wikipedia.org/wiki/Test_de_Ruffier) et [Ruffier-Dickson](https://fr.wikipedia.org/wiki/Test_de_Ruffier#Variante_:_indice_de_Ruffier-Dickson)
- Détente verticale mesurée avec une ceinture d'Abalakov et le test de Sargent
- Licence compétition

## 2. Statistique descriptive

L'objectif de la statistique descriptive est de **résumer** un jeu de données
à l'aide indices (que nous définirons par la suite) afin d'en faciliter la
compréhension.

### 2.1 Statistique univariée

Elle consiste à étudier une seule variable, indépendamment des autres. Cette
variable unique peut ainsi être résumée par des indices de natures différentes. 

#### 2.1.1 Indices de position

Ils rendent compte de la **position** d'une variable dans l'intervalle des valeurs autorisées.

La ***moyenne*** $\mu$ est la somme des valeurs divisée par leur nombre.

$$
\mu = \frac{1}{n}\sum_{i=1}^{n}{x_i}
$$

> :bar_chart: Parenthèse Excel
>
> fonction `MOYENNE(plage)`

La ***médiane*** est la valeur qui sépare la variable en deux parties de même effectif. 
Concrètement, on trie les valeurs de la variable dans l'ordre croissant et on extrait
la valeur à l'indice :
- $(n+1)/2$ si $n$ est impair
- $n/2$ sinon

> :bar_chart: Parenthèse Excel
>
> fonction `MEDIANE(plage)`

> Contrairement à la moyenne, la médiane est peu influencée par des valeurs aberrantes.
> Pour vous en convaincre, calculez la moyenne et la médiane de la variable Age du fichier
> [L1-STAPS.xlsx](data/L1-STAPS.xlsx) et remplacez une des valeurs par 50.

Enfin, le ***quantile $Q_p$*** correspond à la valeur qui sépare les $p\%$ de la variable. Si $p=50\%$, $Q_p$ correspond à la médiane.

Les ***quartiles*** $Q_1$, $Q_2$ et $Q_3$ sont les quantiles correspondant respectivement à $25\%$, $50\%$ (médiane) et $75\%$.

> :bar_chart: Parenthèse Excel
>
> fonction `QUARTILE(plage, quart)`

#### 2.1.2 Indices de dispersion

Ils rendent compte de **l'étalement** des valeurs autour de la moyenne (ou de la médiane).

L'***étendue*** $e$ est la différence entre les valeurs extrémales de la variable.

$$
e = \max_{i}{x_i} - \min_{i}{x_i}
$$

#### 2.1.3 Indice de forme

### 2.2 statistique bivariée

## 3. Statistique inférentielle

L'objectif de la statistique inférentielle est de **généraliser** une observation
réalisée sur un échantillon à l'ensemble de la population. 

### 3.1 Test t de Student

### 3.2 ANOVA