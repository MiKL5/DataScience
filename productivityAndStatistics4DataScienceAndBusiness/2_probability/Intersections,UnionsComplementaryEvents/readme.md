# **Intersections, unions et événements complémentaires**
## **Intersections**
En probalité, une intersection `∩` décrit l’ensemble où deux événements se produisent tous les deux.

Dans un boîte, il y a des boule rouges à gauche (à motifs plein, lignes entrecroisées et rayées) et à droites des boules vertes et bleu rayées.  
On attribue `A` comme l’ensemble de l’événements ou les boules sont rouges, et `B` comme l’événement aux boules rayées ; l’intersection d’`A` et `B`
```js
// L'ordre n'a pas d'importance
A ∩ B = B ∩ A
// Voici la probalité
P(A ∩ B)
// Dans ce cas
P(A ∩ B) = 3/15 = .2
```
<!-- L'intersection est l'ensemble qui se trouve en milieu. -->
## **Unions**
L’union `∪` de deux évènements considère si A ou B (une différence) se produit.
```js
// La non plus l'ordre est sans importance
A ∪ B = B ∪ A
// Cette probabilité est donnée par l'équation
P(A ∪ B) = P(A) + P(B) - P(A ∩ B)
// La probabilité d'A + celle de B - La probabilité de l'intersection d'A et B
P(A ∪ B) = 9/15 + 9/15 - 3/15 = 15/15 = 1.0
```
## **Évènements contraires**
Évènements complémentaire ou contraire `⊼`, il prend en compte tout ce qui est exogène à l’évènement.  
Ici la probabilité de ne pas avoir lévènement A.
```tex
P(⊼) = 1 - P(A) = 15/15 - 9/15 = 6/15 = .4
```
<!-- $$\bar{A}$$ -->
<!-- {\displaystyle {\bar {A}}} -->