# Apprentissage supervisé

Le but est de montrer à la machine des exemples X et Y pour qu'elle trouve l'association qui lie X et Y.

## Dataset

2 types de variables:

- target variable (Y): ce qu'on cherche à prédire
- features (X): les variables qui vont nous aider à prédire Y

on note m le nombre d'exemples et n le nombre de features.
![Alt text](assets\images\apprentissage_supervisé\image.png)
![Alt text](assets\images\apprentissage_supervisé\image-1.png)

## Modèle

Les paramètres du modèle sont les coefficients qui vont permettre de trouver la relation entre X et Y.

![Alt text](assets\images\apprentissage_supervisé\image-2.png)

C'est nous qui décidons du modèle à utiliser. La machine va apprendre les paramètres du modèle.

## Fonction coût

Le modèle va donner des erreurs. La fonction coût va mesurer ces erreurs.

![Alt text](assets\images\apprentissage_supervisé\image-3.png)

Lorsqu'on assemble toutes les erreurs (en rouge), on obtient la fonction coût.

## L'algorithme de minimisation

Le but est de trouver les paramètres du modèle qui minimisent la fonction coût.

exemples d'algorithmes:

- Gradient Descent
- Normal Equation
