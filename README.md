![image](https://github.com/user-attachments/assets/ade29670-903f-4033-9ab8-4ff5fa1f2abc)

Partie 1 : Implémentation en couches avec couplage faible
Dans cette première partie, nous avons pour objectif de mettre en place une architecture orientée vers le principe du couplage faible entre les différentes couches de l’application. Cela permet une meilleure flexibilité, testabilité et maintenabilité du code. Pour cela, les étapes suivantes ont été réalisées :

1. Définition de l’interface IDao
Une interface nommée IDao a été créée afin de représenter la couche d’accès aux données. Cette interface contient une méthode abstraite getData() qui sera par la suite implémentée concrètement dans une classe dédiée.

2. Implémentation de l’interface IDao
Une classe concrète a été développée pour implémenter l’interface IDao. Elle fournit une définition de la méthode getData() et simule un accès aux données, par exemple en retournant une valeur numérique.

3. Définition de l’interface IMetier
Dans le même esprit, une interface nommée IMetier a été définie pour représenter la couche métier de l’application. Cette interface expose une méthode calcul() destinée à effectuer un traitement basé sur les données.

4. Implémentation de l’interface IMetier avec injection de dépendance
Enfin, une classe implémentant l’interface IMetier a été développée. Pour respecter le principe de couplage faible, cette classe ne crée pas elle-même une instance de la couche DAO. À la place, elle reçoit une instance de l’interface IDao via une méthode d’injection (par exemple via un setter ou le constructeur). Cela permet de séparer clairement les responsabilités et de faciliter les tests ou le remplacement de l’implémentation DAO.
