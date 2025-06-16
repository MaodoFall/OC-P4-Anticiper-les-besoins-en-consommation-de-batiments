# 🏙️ Prédiction de la consommation énergétique des bâtiments de Seattle

**Projet 4 – Mastère Spécialisé Data Science – OpenClassrooms**  
**Rôle : Data Scientist**  
**Client : Ville de Seattle**

---

## 🎯 Objectif du projet

Dans le cadre de la **neutralité carbone visée par la ville de Seattle d'ici 2050**, ce projet consiste à prédire :
- La **consommation totale d'énergie** (`SiteEnergyUse(kBtu)`)
- Les **émissions de CO2** des bâtiments non résidentiels

Le but est également d’évaluer l'**intérêt du score ENERGY STAR** dans ces prédictions.

---

## 🗂️ Jeu de données

Source officielle : [Seattle Open Data](https://data.seattle.gov/Built-Environment/Building-Energy-Benchmarking-Data-2015-Present/teqw-tu6e/about_data)  
- **3376 lignes**  
- **46 colonnes** décrivant :  
  - Identifiants des bâtiments  
  - Localisation  
  - Année de construction / rénovation  
  - Type d'usage  
  - Consommation énergétique & émissions

---

## 🧪 Étapes de l'analyse

### 🔍 1. Analyse exploratoire
- Traitement de valeurs manquantes
- Traitement et filtrage des *outliers* grâce à la variable dédiée `Outlier`
- Distribution et transformations (log) sur les cibles

### 🏗️ 2. Feature Engineering
- Sélection des variables pertinentes
- Imputation des valeurs manquantes par **k-plus proches voisins**
- Normalisation des variables
- Deux jeux de données générés : **avec** et **sans** `ENERGYSTARScore`

---

## 🤖 Modèles de prédiction

Pour **chaque tâche (énergie & CO2)**, les modèles suivants ont été testés :
- **Régression linéaire**
- **Forêt aléatoire (Random Forest)**
- **SVR (Support Vector Regression)**
- **XGBoost Regressor**

🔧 **Grid Search** pour l'optimisation des hyperparamètres

---

## 📈 Résultats

### 🔌 Consommation totale d’énergie
- **SVR** = meilleur modèle (plus faible MAPE)

### 🌱 Émissions de CO2
- **XGBoost Regressor** = plus performant
- La **suppression du `ENERGYSTARScore` n'altère pas fortement** les performances → variable peu cruciale

---

## 🔍 Analyse de l'importance des variables
- Importance **globale** : via Random Forest / XGBoost
- Importance **locale** : analyse des prédictions
- Variables dominantes : électricité, gaz et totale d'énergie consommée

---

## 🛠️ Compétences mobilisées

- Prétraitement & transformation des données
- Sélection et évaluation de modèles supervisés
- Régression multivariée avancée
- Optimisation d'hyperparamètres (Grid Search)
- Analyse de l'importance des features
- Comparaison de modèles suivant les métriques adaptées

---

## 📁 Livrables

- 📓 Notebook d'analyse exploratoire des données 
- 📓 Notebook de prédiction de la consommation d'énergie
- 📓 Notebook de prédiction de l'émission de CO2
- 🖥️ Support de présentation

---

## 🙋‍♂️ Réalisé par

**Maodo FALL**  
*Data Scientist*  

---
