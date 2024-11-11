# **Probabilité conditionnelle** <a href="../"><img src="https://github.com/MiKL5/BI/blob/master/assets/bi.svg" alt="Data science" align="right" height="64px"></a>
C’est le fait de valloir connaître la probabilité de l’évènement A, puisse que l’évènement B s’est produit.  
Notée `P(A|B)` et dite `Probabilié d'A, sachant B`.  
La ligne verticale est la manière de noter la probabilié conditionnelle.

Ici on cherche la probabilité de R2 sachant R1
```js
p(R2|R1)  

```
Une fois réorganisée la formule est
```js
P(A ∩ B) = P(A ∩ B) / P(B)
// La proba de A sachant B = à la proba d'A et B divisé par la proba de B
```
<!-- Pour rappel la proba d'A et B est l'intersection d'A et B -->
## Exercice
Une entreprise constate que sur 100 projet, 48 sont achevés dans les délais, 62 en dessous du budget et 16 dans les délais et sous le budget.  
Quand un projet est achevé dans les délais, quelle est la proba qu’il ait été exécuté sous le budget approuvé ?
```js
// IL faut calculer la proba d'A sachant que B s'est produit, donc la proba de l'achevé avec un budget inférieur s'achant qu'il s'est achevé dans les délais
P(A|B) = P(A ∩ B) / P(B)
P(A|B) = 16 / 100 / P48 /100 = 16 / 48 = .33
```