# **Gestion des valeurs manquantes**
Si l’ensemble est incomplet ; l’ensemble rend les prévisions moins précises. Les valeurs manquantes sont traitées avant l’analyse.  
Parmi les méthodes, il y a : 
* la suppression ;
* la complétion par :
  * La moyenne ;
  * La médiane de la colonne ;
  * et cætera.
## **Conversion des types de données**
Permettant que les données soient présentées à l’analyse à un format cohérent, elle est importante.  
E.g. :
* Convertir des colonnes de date en format `date` ;
* transformer des chaînes de caractères en valeurs numériques.
## **Mise à l’échelle des données**
Garantissant que les variables ont une échelle comparable ; simplifiant leur comparaison, est important.  
Les algos tels que le [KNN](https://github.com/MiKL5/Artificial_Intelligence/docs/algo/unsupervisedLearningAlgorithms/KNN) et le [clustering](https://github.com/MiKL5/Artificial_Intelligence/docs/algo/unsupervisedLearningAlgorithms/clustering) utilisant des mesures de distance, l’étape est particulièrement cruciale.