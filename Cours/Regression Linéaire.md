# Régression Linéaire

![Alt text](assets/images/Regression_linéaire/image.png)

Pour la fonction coût, on utilise la `norme euclidienne`.

On prends la moyenne des erreurs au carré. On rajoute un facteur 1/2 pour faciliter les calculs.
![Alt text](assets/images/Regression_linéaire/image-2.png)

Cette fonction coût porte le nom de `Mean Squared Error` (MSE) ou `Erreur Quadratique Moyenne` (EQM).

Méthode des moindres carrés:
![Alt text](assets/images/Regression_linéaire/image-1.png)

Elle implique de faire des inversions de matrices pour obtenir la version de A optimale directement. C'est très coûteux en temps de calcul.
Pour résoudre ce problème, on utilise la méthode de la descente de gradient.

## Descente de gradient

Elle fonctionne pour les courbes de coût `convexes`. (une seule solution optimale)

![Alt text](assets/images/Regression_linéaire/image-3.png)

Cette méthode va permettre de converger vers la valeur de A optimale.

On commence par prendre un paramètre A aléatoire. On va ensuite le modifier petit à petit pour minimiser la fonction coût.

Pour calculer la pente, on calcule la `dérivée partielle` de J(A, B) par rapport à chaque paramètre.

![Alt text](assets/images/Regression_linéaire/image-4.png)

Alpha (α, Learning rate) est le taux d'apprentissage. C'est le pas que l'on va faire pour descendre la pente. Il définit la `vitesse de convergence` de l'algorithme. On dit que c'est un `hyperparamètre`.

On avance de -α \* dérivée partielle pour chaque paramètre. On répète cette opération jusqu'à ce que la pente soit nulle.

![Alt text](assets/images/Regression_linéaire/image-5.png)

La formule de la descente de gradient est la suivante:
![Alt text](assets/images/Regression_linéaire/image-6.png)

### Explication de la formule

- A est le vecteur des paramètres du modèle
- α est le taux d'apprentissage (Il est toujours positif)
- ∇J(A) (A i+1) est le vecteur des dérivées partielles de J(A) par rapport à chaque paramètre

Pour le cas où on se trouve du côté décroissant de la courbe de coût, la dérivée partielle est négative. On avance donc dans le bon sens.
![Alt text](assets/images/Regression_linéaire/image-7.png)

Pour le cas où on se trouve du côté croissant de la courbe de coût, la dérivée partielle est positive. On avance donc dans le sens inverse.
![Alt text](assets/images/Regression_linéaire/image-8.png)

## L'importance du taux d'apprentissage

Si le taux d'apprentissage est trop petit, la descente de gradient va converger très lentement.

Si le taux d'apprentissage est trop grand, la descente de gradient peut ne pas converger du tout.
![Alt text](assets/images/Regression_linéaire/image-9.png)

## Calcul du gradient

![Alt text](assets/images/Regression_linéaire/image-10.png)

![Alt text](assets/images/Regression_linéaire/image-11.png)

![Alt text](assets/images/Regression_linéaire/image-12.png)

## Résumé

![Alt text](assets/images/Regression_linéaire/image-13.png)

## Modèle F

Au lieu de faire le calcul pour chaque valeur de la matrice. On va créer un vecteur F qui va contenir les valeurs de la fonction pour chaque valeur de la matrice.

![alt text](assets/images/Regression_linéaire/part2/image.png)
![alt text](assets/images/Regression_linéaire/part2/image-1.png)

teta est le vecteur des paramètres du modèle. (a et b)

X est la matrice des valeurs de la variable indépendante x.

![alt text](assets/images/Regression_linéaire/part2/image-2.png)
![alt text](assets/images/Regression_linéaire/part2/image-3.png)

## Fonction coût

![alt text](assets/images/Regression_linéaire/part2/image-5.png)

## Gradient

![alt text](assets/images/Regression_linéaire/part2/image-6.png)
![alt text](assets/images/Regression_linéaire/part2/image-4.png)

## Descente de gradient

![alt text](assets/images/Regression_linéaire/part2/image-7.png)

## Regression polynomiale

![alt text](assets/images/Regression_linéaire/part2/image-8.png)

## Résumé

![alt text](assets/images/Regression_linéaire/part2/image-9.png)
