# **Évènements indépendants et dépendants**
## **Les évèneemnts indépendants**
Une série d’évènements indépendants _se produit lorsque le résultat d’un évènement n’a pas d’effet sur le résultat d’un autre_.

Quelle est la probabilité d’obtenir deux Faces en lançant deux fois une pièce de monnaie équilibrée est
```js
P(F1F2) = P(F1) x P(F2) // normalement les chiffres sont en indice
```
Les évènements étant indépendants, la prabalité de Face pour chaque lancer est d’1/2.
```js
P(F1F2) = 1/2 x 1/2 = 1/4
```
Dans le tableau ci-dessous, il y a qu’une combinaison Face/Face.
1er lancer | 2e lancer
:-:|:-:
Face | Face
Face | Pile
Pile | Face
Pile | Pile
## **Les évènements dépendants**
Il se produit si le résultat d’un premier évènement affecte la probalité d’un second évènement.


Si une bille est retirer d’un sac sans être remise ni remplacée affecte la probalité de l’évènement suivant.  
Le sac contient 3 billes rouges et de bleues.  
Quelle est la probabilité que 2 billes sorties du sac soient rouges ?  
La couleur de la première bille va affecter la probabilité d’en sortir une seconde rouge.

Pour la première, c’est facile car sur 5, 3 sont rouges.
```js
P(R1) = 3/5 // il y a 3 possibilité de sortir une première bille rouge
```
La probalité d’en sortir une seconde rouge ; la première été rouge
```js
// La Probabilité P de R2 sachant R1 est essentiellemnt la probalité de R2 connaissant R1 (la première bille était rouge).
P(R2|R1)
// L'ensemble des échantillon étant différent
P(R2|R1) = 2/4
// La probabilité de sortir deux billes rouge
P(R1∩R2) = P(R1) · P(R2|R1)
// Essentiellement que la probalité de l'intersection de R1 et de R2 
// est égale à la probabilité de choisir R1 ou une bille rouge au 1er tirage 
// multiplié par la probabilité de R2 sachant qu'on a l'évènement R1

// Clairement la probalité de choisir 2 billes roucges = la probabilité de choisir une bille rouge au 1er tirage x la probalité d'obtenir une bille rouche lors du second tirage, sachant qu'une bille rouge est sortie au 1er tirage.
P(R1∩R2) = 3/5 x 2/4 = 6/20 = .3
```