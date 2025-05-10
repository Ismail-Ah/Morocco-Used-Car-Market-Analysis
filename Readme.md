# 🚗 Analyse du Marché des Voitures d’Occasion au Maroc pour un Accompagnement à la Prise de Décision

## 📌 Description

Ce projet exploite les données des annonces de voitures d’occasion au Maroc, afin de fournir des analyses permettant aux acheteurs et vendeurs de prendre des décisions éclairées. L’objectif principal est d’estimer le juste prix d’un véhicule, d’éviter les surévaluations ou mauvaises affaires, et de soutenir les négociations grâce à des données objectives.

---

## 🎯 Objectifs

- Estimer le juste prix d’un véhicule en fonction de ses caractéristiques.
- Identifier les facteurs influençant le plus les prix des voitures.
- Déterminer les marques et modèles qui conservent le mieux leur valeur au fil du temps.
- Localiser les villes offrant les meilleures opportunités d’achat.

---

## ❓ Problématique

Le marché des voitures d’occasion au Maroc est dynamique mais souvent opaque, avec des prix incohérents. Les acheteurs et vendeurs manquent de repères fiables pour évaluer la valeur réelle d’un véhicule. Ce projet répond aux questions suivantes :

- Quels sont les facteurs ayant le plus d’impact sur les prix ?
- Comment estimer la valeur d’une voiture à partir de ses caractéristiques ?
- Quelles marques/modèles conservent le mieux leur valeur ?
- Où peut-on trouver les meilleures offres ?

---

## 📊 Données

Le dataset utilisé est disponible sur [Mendeley Data](https://data.mendeley.com/datasets/vjrbcb2rrt/2). Le fichier principal est `cars_dataframe.csv`, contenant :

- Marque, Modèle  
- Année du modèle  
- Kilométrage  
- Ville, Secteur  
- Carburant, Boîte de vitesses, Nombre de portes  
- Équipements (GPS, cuir, climatisation, etc.)  
- État, Première main, Origine  
- Prix  

---

## 🤖 Modèle d'IA

Ce projet utilise le machine learning pour prédire le prix d’un véhicule d’occasion à partir des caractéristiques mentionnées ci-dessus. Les modèles entraînés incluent :

- XGBoost  
- CatBoost  
- LightGBM  
- Régression Ridge  

Un système de recommandation est également intégré pour suggérer des véhicules selon les préférences des utilisateurs.

---

## 🧰 Prérequis

- Python 3.11+
- Bibliothèques : `pandas`, `numpy`, `scikit-learn`, `catboost`, `xgboost`, `lightgbm`, `category_encoders`, `matplotlib`, `seaborn`, `joblib`
- Fichier de données : `cars_dataframe.csv`
- Modèles pré-entraînés (optionnels) :
  - `best_lightgbm_model.pkl`
  - `best_catboost_model.pkl`
  - `best_xgb_model.pkl`
  - `best_ridge_model.pkl`

---

## ⚙️ Installation

```bash
# Cloner le dépôt
git clone https://github.com/Ismail-Ah/Morocco-Used-Car-Market-Analysis.git
cd Morocco-Used-Car-Market-Analysis

# Installer les dépendances
pip install -r requirements.txt

## 🚀 Exécution

1. Lancez le notebook Jupyter ou le script Python.
2. Chargez le fichier `cars_dataframe.csv`.
3. (Optionnel) Assurez-vous que les modèles `.pkl` sont présents pour éviter de réentraîner.
4. Suivez les étapes dans l’ordre :

   * Section 0 : Installation des packages.
   * Section 1-2 : Importation et nettoyage des données.
   * Section 3 : Analyse exploratoire.
   * Section 4-6 : Prétraitement, ingénierie des variables, encodage.
   * Section 7-8 : Gestion des outliers, imputation, sélection des features.
   * Section 9-10 : Split, entraînement des modèles.
   * Section 11-12 : Évaluation et visualisation.

---

## 📈 Résultats

Les modèles ont été évalués selon plusieurs métriques (RMSE, MAE, MAPE, R²). Résumé des performances sur les données de test :

| Modèle           | RMSE      | R²     |
| ---------------- | --------- | ------ |
| XGBoost          | 24 805.95 | 0.8828 |
| LightGBM         | 25 229.64 | 0.8787 |
| CatBoost         | 26 706.92 | 0.8641 |
| Régression Ridge | 49 729.78 | 0.5288 |

📊 Les visualisations comprennent :

* Graphiques de prédiction vs valeur réelle
* Importance des variables
* Analyse des résidus

---