# **L’algorythme Depth-first search DFS**<a href="../../"><img src="../../assets/atomicDs.png" alt="Data science" align="right" height="64px"></a>
L’algorythme de parcours en profondeur, parcours les arbres et plus souvent les graphes.  
Il est récursif. Son utilisation la plus simple consiste à déterminer l’existance d’un chemin d’un bout à l’autre.

Concernant les graphes non orientés, le parcours en profondeur correspond à la méthode intuitive utiliser pour trouver la sortie d’un labyrinthe sans passer deux fois au même endroit.  
C’est dés le XIXème siècle, que les premiers parcours en profondeurs sont formulés. 
## **Le principe**
L’exploration d’une DFS depuis un sommet (ou noeud) S poursuit un chemin dans le graphe jusqu’à une voie sans issue ou le sommet déjà visité. Il repart du dernier sommet où il peut suivre, puis explorer un autre chemin. En conséquence l’exploration prend fin quand tous les sommet depuis S ont été visités. Donc, l’exploration progresse récursivement d’un sommet S en s’appelant récursivement pour chaque sommet voisins à S.

Son nom vient du fait que contrairement à l’[algo de parcours en largeur](../bfs), il explore tous les chemins un à un. À chaque sommet, ii marque l’actuel sommet ; prend le premier sommet voisin jusqu’à ce qu’il n’y ait plus de sommet voisin ou que tous soient marqués ; revient au sommet père.  
Si G n’est pas un arbre, l’algo marque les sommets visités de façon à ne pas les ré-explorer. Par ailleurs, le DFS caractérise l’abre quand sa mission est de parcourir un arbre.
## **Les applications**
À l’instar des autres parcours de graphe, le DFS trouve l’ensemble des sommet accessibles au départ d’un sommet défini (nommé S). Ceci s’applique à un graph qu’il soit orienté ou non. Pour un graphe non orienté, utilisé cette propriété permet le calcul des compasants connexes.  
Dans le cadre d’un graphe orienté acyclique, le DFS sert au calcul de tri topologique des sommets.

L’[algo de Kosaraju](../kosaraju) fait un double DFS pour déterminer les composants fortement connexes d’un graphe orienté quelquonque.
## **Le complexité**
La complexité du parcours en temps est <b><kbd>_O_(|S|+|A|)</kbd></b>. <kbd>|S|</kbd> est le nombre des sommets. <kbd>|A|</kbd>, le nombre d’arcs.  
Si les parcours en profondeur est lexicographique<!-- (ordre défini sur les suites finies d'éléments d'un ensemble ordonné)-->, il est difficilemnt parallélisable. Nonobstant, avec les machines probailistes et dans les classes RNC, il est parallelistable.