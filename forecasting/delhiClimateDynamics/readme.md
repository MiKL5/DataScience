# **Analyse des dynamiques climatiques de Delhi**<a href="../../"><img src="../../assets/atomicDs.png" alt="Data science" align="right" height="64"></a>
<a href="../../"><img src="../../assets/dailyClimateDynamics.png"></a>

Étude des séries temporelles climatiques de la ville de Delhi.  
Modéliser et de comprendre les interactions dynamiques entre la température, l'humidité et la vitesse du vent par une approche économétrique.
---

<div align="center">

![Python](https://img.shields.io/badge/Python-3.13-3776AB?style=flat&logo=python&logoColor=white) 
![pandas](https://img.shields.io/badge/pandas-2.3.3-150458?style=flat&logo=pandas&logoColor=white) 
![scikit--learn](https://img.shields.io/badge/scikit--learn-1.8.0-F7931E?style=flat&logo=scikit-learn&logoColor=white) 
![Statsmodels](https://img.shields.io/badge/Statsmodels-0.14.6-7193c1?style=flat&logo=statsmodels&logoColor=white) 
![Quarto](https://img.shields.io/badge/Quarto-1.7.29-4758AB?style=flat&logo=quarto&logoColor=white) 
![JupyterNotebook](https://img.shields.io/badge/JupyterLab-4.3.5-F37626?style=flat&logo=Jupyter&logoColor=white)

</div>

## **L'objectifs du Projet**
L'étude s'articule autour de deux axes :
1. La **modélisation Univariée (SARIMA)**  
   ➜ Capture de la composante saisonnière annuelle et prévision de la température moyenne.
2. L'**analyse Systémique (VAR)**  
   ➜ Étude des rétroactions entre variables climatiques après vérification de l'antériorité informative (Causalité de Granger).
## **La méthodologie**
* Le **prétraitement**  
  ➜ Agrégation mensuelle des données journalières pour extraire le signal climatique.
* La **stationnarisation**  
  ➜ Utilisation du test de Dickey-Fuller Augmenté (ADF) et application de différenciations saisonnières.
* La **sélection de Modèle**  
  ➜ Arbitrage entre complexité et fidélité via le principe de **parcimonie** (Critère AIC).
* M'**interprétation**  
  ➜ Analyse des fonctions de réponse impulsionnelle (**IRF**) sur données standardisées.
## **Les principaux Résultats**
* Mise en évidence d'une **stabilité systémique** ➜ le retour à l'équilibre après un choc climatique s'opère sous 6 à 8 mois.
* Validation d'une **causalité au sens de Granger** de l'humidité sur la température, confirmant l'interdépendance des variables atmosphériques.
* Modèle final retenu ➜ **VAR(1)** pour sa robustesse statistique.
## **Le Workflow de l'Étude**
```mermaid
graph TD
    %% Définition des styles
    classDef source fill:#34495e,stroke-width:0px,color:white;
    classDef process fill:#003747,stroke-width:0px,color:white;
    classDef decision fill:#d53600,stroke-width:0px,color:white;
    classDef model fill:#1c0333,stroke-width:0px,color:white;
    classDef result fill:#030,stroke-width:0px,color:white;
    classDef output fill:#7c501a,stroke-width:0px,color:white,stroke-dasharray:5 5;

    A["Données brutes\<br/>DailyDelhiClimate.csv"] --> B["Agrégation mensuelle"]
    B --> C{"Analyse statistique"}

    C --> D["Volet univarié\<br/>SARIMA"]
    C --> E["Volet multivarié\<br/>VAR"]

    D --> D1["Test ADF & différenciation"]
    D1 --> D2{"Identification SARIMA\<br/>(1,1,1) × (1,1,1)\u2081\u2082"}

    E --> E1["Causalité de Granger\<br/>& sélection"]
    E1 --> E2["Standardisation\<br/>StandardScaler"]
    E2 --> E3{"Arbitrage & parcimonie\<br/>VAR(1)"}

    D2 --> F{"Synthèse des dynamiques"}
    E3 --> F

    F --> G["Interprétation des IRF"]
    G --> H["Publication\<br/>Quarto HTML report"]

    %% Application des classes
    class A source;
    class B,D,E,D1,E1,E2 process;
    class C,F decision;
    class D2,E3 model;
    class G result;
    class H output;
```
___
_Projet d'analyse de série temporelle réalisé dans un cadre académique_.