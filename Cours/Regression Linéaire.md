# Régression Linéaire

![Alt text](image.png)

Pour la fonction coût, on utilise la `norme euclidienne`.

On prends la moyenne des erreurs au carré. On rajoute un facteur 1/2 pour faciliter les calculs.
![Alt text](image-2.png)

Cette fonction coût porte le nom de `Mean Squared Error` (MSE) ou `Erreur Quadratique Moyenne` (EQM).

Méthode des moindres carrés:
![Alt text](image-1.png)

Elle implique de faire des inversions de matrices pour obtenir la version de A optimale directement. C'est très coûteux en temps de calcul.
Pour résoudre ce problème, on utilise la méthode de la descente de gradient.

## Descente de gradient

Elle fonctionne pour les courbes de coût `convexes`. (une seule solution optimale)

![Alt text](image-3.png)

Cette méthode va permettre de converger vers la valeur de A optimale.

On commence par prendre un paramètre A aléatoire. On va ensuite le modifier petit à petit pour minimiser la fonction coût.

Pour calculer la pente, on calcule la `dérivée partielle` de J(A, B) par rapport à chaque paramètre.

![Alt text](image-4.png)

Alpha (α, Learning rate) est le taux d'apprentissage. C'est le pas que l'on va faire pour descendre la pente. Il définit la `vitesse de convergence` de l'algorithme. On dit que c'est un `hyperparamètre`.

On avance de -α \* dérivée partielle pour chaque paramètre. On répète cette opération jusqu'à ce que la pente soit nulle.

![Alt text](image-5.png)

La formule de la descente de gradient est la suivante:
![Alt text](image-6.png)

### Explication de la formule

- A est le vecteur des paramètres du modèle
- α est le taux d'apprentissage (Il est toujours positif)
- ∇J(A) (A i+1) est le vecteur des dérivées partielles de J(A) par rapport à chaque paramètre

Pour le cas où on se trouve du côté décroissant de la courbe de coût, la dérivée partielle est négative. On avance donc dans le bon sens.
![Alt text](image-7.png)

Pour le cas où on se trouve du côté croissant de la courbe de coût, la dérivée partielle est positive. On avance donc dans le sens inverse.
![Alt text](image-8.png)

## L'importance du taux d'apprentissage

Si le taux d'apprentissage est trop petit, la descente de gradient va converger très lentement.

Si le taux d'apprentissage est trop grand, la descente de gradient peut ne pas converger du tout.
![Alt text](image-9.png)

## Calcul du gradient

![Alt text](image-10.png)

![Alt text](image-11.png)

![Alt text](image-12.png)

## Résumé

![Alt text](image-13.png)
