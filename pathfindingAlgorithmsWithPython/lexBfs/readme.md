# **L’algo LexBFS** <a href="../../"><img src="../../assets/atomicDs.png" alt="Data science" align="right" height="64px"></a>
Cet algo de théorie des graphes est un parcours lexicographique en largeur. Par conséquent, un rafinement du BFS.
## **Contexte**
Usuellement le BFS :
> Initialise une liste de sommets avec des noeuds de départ comme unique élément de la file ;  
> Tant que la file n’est pas vide, retirer (défiler) le sommet, marquer et ajouter à la file (enfiler) tous les sommets voisins non marqués à une antérieure étape.

Cependant, le sommet peut être défini déclarativement par les propriétés de ses sommets. Le parcours en lageur standard est produit par l’itération de cette règle :
> À chaque étape choisir le sommet non choisi, dont l’ensemble des prédécesseurs a été choisi au plus tôt possible.

Parfois, l’ordonancement des sommets par l’orde de choix de leurs prédécesseurs peut mener à des égalités (plusieurs peuvent avoir le même prédécesseur). L’ordre arbitraire intervient. L’ordre de choix du LexBFS diffère en résolvant les égalités par une règle systématique.
> Grâce à la lexicographie, à chaque étape, le sommet n’ayant pas été choisi dont l’ensemble des prédécesseurs choisis est aussi petit que possible.

LexBFS, peut donc choisir celon du second prédécesseur.

⚠️ Utiliser cette règle d’ordonancement directement rend l’algo inéficace ; LexBFS utilise une structure de données adaptée pour produire efficacement l’odonancement, comme un parcours stantard de largeur utilise aussi une structure de données de file pour déterminé efficacement l’ordre.
## **Son application**
Il permet notamment de reconnaître les graphes cordaux en temps linéaire.