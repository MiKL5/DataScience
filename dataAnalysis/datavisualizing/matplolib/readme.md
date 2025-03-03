# **Matplotlib**
La visualisation de données (data visualiation ou data viz) est une composante essentielle de l’analyse de données moderne ; les informations complexes sont représentées visuelement mettant en évidence des schémas, des tendances et des relations cachées.  
C’est l’un des outils les plus populaires en data viz.
## **Définition**
C’est une bibliothèque de visualisation de données (développée dans les années 2000 par John HUNTER) en Python inspirée de matlab. Ce neurobiologiste cherchait un moyen de visualiser les signaux électriques cérébraux des patients épileptiques. En 2012, suite au décès de son créateur, de nombreux contributeurs ont alimenté ce projet open source.

Cette bibliothèque complète et populaire, et permet la création de visualisations statiques, animées et interactives. Pouvant générer des graphiques en `pdf`, `svg`, `png`, `jpg`, `bmp` et `gif`. Prisé par les utilisateurs de Python et Numpy, et souvent utilisé dans les serveurs d’applications web, shells et des scripts Python.

Les API de matplolib permettent aux développeurs d’intégrer des graphiques dons les applications d’interface graphiques, ajoutant une dimension visuelle.
## **Comment fonctionne t-elle ?**
De deux façons : via la POO ou le module Pyplot.
### **En POO**
Cette approche peremt de créer les figures et axes explicitement. En suite, sont appelées les méthodes associées pour tracer les graphiques.
```py
import matplolib.pyplot as plt

# Création de la figures et des axes
fig.ax = plt.subplots()

# Traçage des données
x = [1 , 2 , 3 , 4 , 5]
y = [2 , 4 , 6 , 8 , 10]
ax.plot(x,y,label='Données')

# Personnalisation du graphique
axset_title('Exemple de tracé via le dév orienté objet')
axset_xlabel('Axe X')
axset_ylabel('Axe Y')
axlegend()

# Affichage de graphique
plt.show()
```
### **Avec Pyplot**
Ce module a une interface analogue à `Matlab`, nonobstant, la création de graphique est plus simple et concise.
```py
import matplolib.pyplot as plt

# Traçage des données
x = [1 , 2 , 3 , 4 , 5]
y = [2 , 4 , 6 , 8 , 10]
ax.plot(x,y,label='Données')

# Ajout des titres et étiquettes
plt.title('Tracé via Pyplot')
plt.xlabel('Axe X')
plt.ylabel('Axe Y')
plt.legend()

# Affichage du graphique
plt.show()
```
## **Les principaux composants de Matplolib**
Elle repose sur plusieurs composants clés faciliant la création de graphiques et la visualisation de grande qualité.
### **La figure**
C’est un conteneur de premier niveau pour tous les éléments ou artistes composants l’image graphique. Le plus s’imple moyen est `pyplot`.
* Figure sans axe : `fig = plt.figure()` ;
* Figure à 1 axe : `fig.ax = plt.subplots()` ;
* Figure à grille 2x2 axes : `fig.axs = plt.subplots(2 , 2)` ;
* Figure à 1 axe gauche et 2 droits : `fig.axs = plt.subplots_mosaic( [ ['left' , 'right_top'] , ['left' , 'right_bottom'] ] )`.
### **Les artistes**
Parmis eux, il y a la figure, les axes, les lignes, les textes, les légendes, le fond et la grille.  
Chacun est personnalisable en modifiant les propriétés (e.g. : couleur, style, taille, position), permettant un total contrôle de l’apparence et du contenu des graphiques.
### **Les axes**
C’est un **artiste attaché à une figure** contenant un espace de traçage des données. Il comprend généralement 2 objets Axis (ou 3 en 3D) fournissants des repères ou ticks. Chacun possède :
* un titre, `set_title()` ;
* une étiquette x, `set_xlabel()` ;
* une étiquette y, `set_ylabel()`.
### **Les axis**
Ils définissent l’**échelle et les limites du tracé** générants des ticks sur l’axe et ont étiquetés par les **tickslabels**. L’emplacement est déterminé avec l’objet Locator et les tickslabels sont formatés par un Formatter, avec l’interface `set_xticks`<!-- :-->
<!--```py
fig.axs = plt.subplots(2 , 1 , layout = 'constained')
axs[0].plot(xdata , data1)
axs[0].set_title('Automatic ticks')
axs[1].plot(xdata , data1)
axs[1].set_xticks(np.arange(0 , 100 , 30) , ['zero' , '30' , 'sixty' , '90'] )
axs[1].set_yticks( [-1.5 , 0 , 1.5] )
axs[1].set_title('Manual ticks').
```
-->
### **Les ticks**
Ces repères servent à **spécifier les positions** et les étiquettes des marques sur les axes. Les **fonctions `set_xticks` et `set_yticks`** permettent de définir les positions des repères sur les axes x et y<!-- (e.g. : `plt.xticks( [1 , 2 , 3 , 4 , 5] , ['A' , 'B' , 'C' , 'D' , 'E'] )`)-->.

<!-- Les `set_xtickslabel` ou `set_ytickslabel`.  
`x = np.linspace(0 , 2 * np.pi , 100)`  
`y = np.sin(x)`

Les données sont tracés se font par `plp.plot(x , y)`. Des **repères personnalisés** peuvent être définis avec plt.xticks( [ 0 , np/pi , 2*np.pi] , ['0' , '$\pi$' , '2$\pi$'] ). -->