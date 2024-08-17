# **Le théorème de Bayes**
Ce théorème est utiliser en médecine par des outils de diagnostique (cancer, …), et cetains business.

Si les deux formules de proba conditionnelle sont reliées cela donne le théorème de Bayes.
<a href="#"><div align="center"><img src="../../assets/bayes.jpg" height="96px"></div></a>
La proba que l’évt A sachant B est égale à la proba de B sachant A, multiplier par la proba d’A sur la proba de B, à condition que la proba d’A et celle de B soient toutes les 2 supérieures 0.

Précisément le théorème de Bayes est utilisé pour déterminé la proba d’un paramètre, compte tenu d’un certain évènement.  
La formule réelle est
<a href="#"><div align="center"><img src="../../assets/bayesGenerale.jpg" height="96px"></div></a>
Les 2 proba conditionneles de B sachant A et d’A sachant B sont reliées.
### Exxercice
Dans l’entreprise 1 produit sur 500 est déféctueux soit .2%.  
L’entreprise a acheter un outil de diagnostique identifiant correctement une pièce défectueuse à 99%.  
Quelle est la proba qu’une pièce défectueuse le soit réellement ?  
A = proba d’être defectueuse  
B = proba que le test soit positif  
```js
P(A|B) = "proba d'être défectueuse si le test est positif" = ?
P(B|A) = "proba d'un test positif en cas de défaut"        = .99
P(A)   = "proba d'être défectueuse"                        = .002
P(B)   = "celle que le test soit positif"                  = besoin de la calculer
// Il y aura un vrai positif et un faux positif
P(B) = proba d'un test positif
     = P(vrai positif) + P(faux positif)
     = P(B|A) · P(A) + P(B|-A) · P(-A) = la proba de B sachant A x la proba de A défectueux + proba d'un faux positif x la proba qu'il ne soit pas défectueux

P(B|-A) = 1 - P(B|A) = 1 - .99 = = .01 d'être défectueux
P(-A) = 1 - P(A) = 1 - .02 = .998 d'être sain"
```
<a href="#"><div align="center"><img src="../../assets/bayesBigVersion.jpg" height="96px"></div></a>
```js
= .99 x .002 / .99 x .002 + .01 x .998
= .165
```
Il n’y a que 16,5% de proba d’identifier correctement une pièce défectueuse.
```js
// Avec un second test
= .99 x .165 / .99 x .165 + .01 x .835
= .951
```
Deux tets positifs indiques qu’il y a 95,1% de proba que le diag indique qu’elle est defectueuse.