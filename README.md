# Clustering des pratiques agricoles : Cohorte Agrican 1960 🚜

Ce projet, réalisé dans le cadre de la **SAE 4.02** (Bachelor Universitaire de Technologie en Science des Données), porte sur le reporting d'une analyse multivariée appliquée à la cohorte épidémiologique **Agrican** (Agriculture et Cancer).

## 📋 Présentation du projet
L'objectif est de définir des profils types d'agriculteurs en fonction des activités pratiquées durant leur carrière professionnelle pour la sous-cohorte 1960 (individus ayant débuté entre 1950 et 1970). 

### Population d'intérêt
* **Effectif total** : 12 310 agriculteurs.
* **Variables** : Ratios de pratique par activité (Bovins, Vigne, Blé, Maïs, etc.), durée de carrière, et données démographiques/santé (tabagisme).

---

## 📊 Méthodologie Statistique

### 1. Analyse en Composantes Principales (ACP)
L'ACP a été utilisée pour réduire la dimensionnalité des 13 variables d'activité tout en synthétisant l'information :
* **Inertie conservée** : Environ **76%** de l'information initiale est expliquée par les 7 premiers axes factoriels.
* **Interprétation des axes** : L'axe 1 oppose les grandes cultures et l'élevage bovin aux cultures spécialisées.

### 2. Classification Automatique (K-means)
Une segmentation de la population a été réalisée via la méthode des k-means :
* **Nombre de clusters** : 5 clusters optimaux identifiés grâce à la **méthode du coude**.
* **Critère** : Analyse de l'évolution de l'inertie d'interclasse pour maximiser l'homogénéité au sein des groupes.



---

## 🚀 Résultats Clés

### Profilage des Clusters
L'étude a permis d'identifier des spécialisations agricoles marquées :
* **Cluster 2 (Bovins)** : Spécialisation quasi-exclusive dans l'élevage bovin (ratio moyen de 94,08).
* **Cluster 6 (Vignes)** : Profils viticoles avec un ratio de pratique de 96,99.
* **Cluster 4 (Céréales & Carrières longues)** : Dominé par les prairies (85,45%) et le blé, avec la durée de carrière moyenne la plus longue (36,69 ans).

### Analyse de Santé
* Le clustering a mis en évidence des disparités comportementales : le **cluster 5** présente la proportion de fumeurs la plus élevée (**58%**), contre **46%** pour le cluster 4.

---

## 🛠️ Outils utilisés
* **Langage R** : Traitement des données, ACP (`FactoMineR`), Clustering (`stats`).
* **Visualisation** : `ggplot2` pour l'analyse de l'inertie et des corrélations.
* **Reporting** : Rapport structuré détaillant le calcul des matrices de ratios.



---
*IUT Grand Ouest Normandie - Campus de Lisieux*