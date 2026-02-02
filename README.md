# End-to-End-Machine-Learning-System-for-ICU-Patient-Survival-Prediction

## Table des matières
1. [Contexte du projet](#1-contexte-du-projet)
2. [Objectifs du projet](#2-objectifs-du-projet)
3. [Présentation du dataset](#3-présentation-du-dataset)
4. [Méthodologie proposée](#4-méthodologie-proposée)
5. [Modèles de Machine Learning](#5-modèles-de-machine-learning-envisagés)
6. [Évaluation des performances](#6-évaluation-des-performances)
7. [Interprétabilité et explicabilité](#7-interprétabilité-et-explicabilité)
8. [Outils et technologies](#8-outils-et-technologies)
9. [Résultats attendus](#9-résultats-attendus)
10. [Perspectives d’évolution](#10-perspectives-dévolution)
11. [Conclusion](#11-conclusion)
12. [Objectifs détaillés (SMART)](#12-objectifs-détaillés-smart)
13. [Justification du choix du dataset](#13-justification-du-choix-du-dataset)
14. [Données additionnelles (optionnelles)](#14-données-additionnelles-optionnelles)
15. [Définition du problème Machine Learning](#15-définition-du-problème-machine-learning)
16. [Métriques de performance retenues](#16-métriques-de-performance-retenues)
17. [Pipeline Machine Learning](#17-pipeline-machine-learning-détaillé)
18. [Architecture technique](#18-architecture-technique)
19. [Sécurité & robustesse](#19-sécurité--robustesse)
20. [Organisation du travail (7 semaines)](#20-organisation-du-travail-7-semaines)
21. [Livrables attendus](#21-livrables-attendus)
22. [Critères de réussite](#22-critères-de-réussite)
23. [Conclusion générale](#23-conclusion-générale)

---

## 1. Contexte du projet
Le secteur de la santé adopte massivement la **Data Science et le Machine Learning**, notamment pour l’aide à la décision médicale. Ce projet utilise le dataset **SUPPORT2 – UCI** pour prédire la survie des patients en soins intensifs et analyser les facteurs de risque.

Objectifs professionnels :  
- Analyse de données médicales réelles  
- Modélisation prédictive  
- Interprétabilité des modèles (*explainable AI*)  

---

## 2. Objectifs du projet

### Objectif principal
Développer un **modèle de prédiction de survie en soins intensifs** à partir de données cliniques et biologiques.

### Objectifs secondaires
- Identifier les **facteurs médicaux les plus influents**  
- Comparer plusieurs modèles ML  
- Évaluer la performance avec métriques adaptées  
- Fournir une interprétation claire pour un usage décisionnel  

---

## 3. Présentation du dataset
- **Nom** : SUPPORT2  
- **Source** : UCI ML Repository  
- **Type** : Données tabulaires médicales  
- **Observations** : ~9 100 patients  
- **Variables** : ~42 (démographiques, cliniques, biologiques)  
- **Cible** : survie / décès  

---

## 4. Méthodologie proposée

### 4.1 Analyse exploratoire (EDA)
- Analyse descriptive  
- Visualisation des distributions  
- Corrélations  
- Valeurs manquantes  

### 4.2 Prétraitement
- Imputation des valeurs manquantes  
- Encodage catégoriel  
- Normalisation / standardisation  
- Gestion du déséquilibre (SMOTE, class weights)  

---

## 5. Modèles de Machine Learning envisagés

### Baseline
- Logistic Regression  
- Decision Tree  

### Avancés
- Random Forest  
- Gradient Boosting (XGBoost / LightGBM)  
- SVM  

### Optionnels
- Neural Network (MLP)  
- Survival Analysis (Cox PH Model)  

---

## 6. Évaluation des performances
- Accuracy (indicatif)  
- Precision / Recall (priorité médicale)  
- F1-score  
- ROC-AUC  
- Confusion Matrix  

Validation : Cross-validation, comparaison des modèles  

---

## 7. Interprétabilité et explicabilité
- Analyse de l’importance des variables  
- SHAP values  
- Visualisation des contributions  

---

## 8. Outils et technologies
- **Langage** : Python  
- **Librairies** : pandas, numpy, scikit-learn, matplotlib, seaborn, xgboost/lightgbm, shap  

---

## 9. Résultats attendus
- Modèle performant  
- Rapport détaillé  
- Visualisations claires  
- Interprétation médicale  

---

## 10. Perspectives d’évolution
- Données temporelles (time-series)  
- Déploiement (Streamlit)  
- Comparaison avec autres hôpitaux  
- Intégration de règles médicales (hybrid AI)  

---

## 11. Conclusion
Application professionnelle du ML en santé, axée sur performance, robustesse et interprétabilité.  

---

## 12. Objectifs détaillés (SMART)
- Pipeline ML complet (data → modèle → API → UI → Docker)  
- Bonnes pratiques MLOps (MLflow, versioning, reproductibilité)  
- Gestion du déséquilibre  
- Comparaison des modèles  
- Interprétation médicale  

---

## 13. Justification du choix du dataset
- **Nom** : SUPPORT2  
- Données réelles, complexité élevée, cas critique, validé académiquement  

---

## 14. Données additionnelles (optionnelles)
- Données démographiques agrégées  
- Indicateurs statistiques dérivés  
- Simulations pour tests API  

> ⚠️ Respect de l’éthique, pas de données sensibles supplémentaires  

---

## 15. Définition du problème Machine Learning
- Classification binaire  
- Variable cible : 0 = survivant, 1 = décès  
- Priorité : minimiser faux négatifs, privilégier Recall & ROC-AUC  

---

## 16. Métriques de performance retenues
- Recall  
- Precision  
- F1-score  
- ROC-AUC  
- Confusion Matrix  

---

## 17. Pipeline Machine Learning détaillé
1. Ingestion des données  
2. EDA  
3. Nettoyage & prétraitement  
4. Feature engineering  
5. SMOTE  
6. Entraînement  
7. Optimisation (GridSearchCV)  
8. Tracking MLflow  
9. Sélection modèle  
10. Sérialisation  

---

## 18. Architecture technique
**Backend** : FastAPI, Pydantic, REST  
**Frontend** : React + Vite, Dashboard interactif  
**Déploiement** : Docker, Docker Compose, services isolés  

---

## 19. Sécurité & robustesse
- Validation API  
- Gestion des erreurs  
- Logs  
- Health checks  

---

## 20. Organisation du travail (7 semaines)
- S1 : Setup, EDA  
- S2 : Preprocessing, SMOTE  
- S3 : Modélisation & MLflow  
- S4 : Backend  
- S5 : Frontend  
- S6 : Dockerisation  
- S7 : Revue finale & CI/CD  

---

## 21. Livrables attendus
- Code source  
- API fonctionnelle  
- Interface utilisateur  
- Conteneurs Docker  
- Rapport technique  
- Dépôt GitHub documenté  

---

## 22. Critères de réussite
- Pipeline ML fonctionnel et traçable  
- Modèle interprétable  
- Déploiement réussi via Docker  
- Documentation claire  

---

## 23. Conclusion générale
Projet complet, aligné avec standards industriels ML, combinant rigueur scientifique, bonnes pratiques MLOps et mise en production.

