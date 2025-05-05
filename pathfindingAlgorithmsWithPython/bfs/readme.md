# **L’algo de parcours en largeur BFS** <a href="../../"><img src="../../assets/atomicDs.png" alt="Data science" align="right" height="64px"></a>
Le but du Breath First Search est de parcourir un graphe ou arbre par l’exploration d’un noeud, puis les successeurs, … Cette algo permet le calcul des distances de tous les noeuds depuis un noeud source dans un graphe non pondéré (orienté ou pas). Si un graphe est non orienté et connexe, il peut le déterminé.
## **Son principe**
Un BFS commence au noeud source & liste tous les voisins afin d’explorer les autres 1 à 1. Il y a donc une file dans laquelle le premier sommet est au début et les voisins à la suite, en dernier les voisins non encore exploités. Chaque noeud visiter est marqué pour ne pas y repasser. Sauf pour un arbre ; la marquage n’est pas nécessaire.
1. Le noeud source est dans la file ;
2. Retire le noeud du début de la file et la traiter ;
3. Mette tous les voisins non explorés à la fin de la file ;
4. Tant que la file n’est pas vide réitérer à l’étape 2.
## **DFS vs BFS**
DFS | BFS
 :-:|:-:
Explore lexicographiquement<br>tant qu’il y a une issu<br>et revient à un autre noeud | Suit la file tant qu’elle n’est pas vide
Son principe repose sur un pile | Le sien sur une file
## **La complexité**
Dans le pire des cas <kbd>_O_(|S|+|A|)</kbd>. Chaque sommet a une unique visite. Soit un graphe `G=(S , A)`, dont aucun somme n’est marqué à l’appel de l’algo. Chaque sommet de la file sont marqués, ainsi l’intruction conditionnelle assure que les sommets sont insérés qu’une fois.
## **Son utilisation**
Le BFS (parcours en largeur) explore l’intégralité des sommets accessibles depuis le sommet source. Cet algo est conçu pour le calcul des composantes connexes d’un graphe non orienté avec une complexité linéaire en la taille du graphe.

Par ailleurs, les sommets sont explorés par distance croissante au sommet source. Grâce à ça, il est possible d’utiliser cet algo à la résolution de :
* Trouver les plus courts chemins.

L’[algo de Djikstra](https://github.com/MiKL5/Artificial_Intelligence/blob/master/docs/algo/Dijkstra) peut être assimiler a un parcours BFS dont les arcs sont pondérés positivement.

[LexBFS](../lexBfs) permet la reconnaissance rapide de certaines classes de graphes.