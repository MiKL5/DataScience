# **L’algorythme de Kosaraju** <a href="../../"><img src="../../assets/atomicDs.png" alt="Data science" align="right" height="64px"></a>
Sambasiva Rao Kosaraju est un informaticien et prof américain d’informatique à l’université John Hopkins en Pensylvanie, exerçant à la conception et l’analyse d’algos séquentiels et parallèles.  
L’algo de Kosaraju de calcul des composantes fortement connexes d’un graphe fortement orienté et éponymement nommé.
## **L’algo**
Il sert au calcul des composantes fortement connexes d’un graphe orienté ; effectuant 2 DFS et a une complexité linéaire en la taille du graphe.
## **Sa déscription**
Le graphe est ‘G’. L’algo est en 2 étapes. DFS est exécuter à ‘G’ et le post’ordre est noté (c-à-d l’ordre suffixe ou de remontée). Puis DFS aux graphe transposé noté (G exposant t) en suivant l’ordre obtenu à la permière étape.  
En conséquence, les arbres obtenus par le second DFS sont des [composantes fortement connexes (CFC)](cfc).