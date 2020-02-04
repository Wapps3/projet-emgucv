Bloquer :

La co-routine qui détecte les inputs appelle une fonction qui détecte la zone du bouclier.
Cette fonction détecte les plus grand contours de la couleur définit par les paramètre du bouclier.
Ensuite la fonction calcul l'air du plus grand contour (si il existe).
Si cette air dépasse une valeur seuil alors la fonction renvoie true, ce qui déclenche l'action de bloquer.
L'action de bloquer à la priorité sur l'action de frapper.

Frapper :

La co-routine qui détecte les inputs appelle une fonction qui renvoie si le personnage attaque ou non.
Et dans l'objet qui détecte l'épée il y a une fonction qui met à jour ce booléen d'attaque. 
Cette fonction est appellé toutes les 0.5 secondes. Elle détecte le contour le plus grand de la couleur définit par les paramètres de l'épée.
Ensuite la fonction calcul le centroid du contour, puis elle calcul la distance entre ce nouveau centroid et le précédent.
Si la distance est suffisant grand alors elle set le booléen à true sinon à false.


Piste d'amélioration :

Rendre possible la modification des paramètres de couleur de l'épée et du bouclier directement dans le jeu.
Se baser plutot sur le mouvement de l'épée plutôt que sur le déplacement de son centroid.
