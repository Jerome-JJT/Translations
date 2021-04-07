Les nombres aléatoires sont souvent utilisés pour la programmation de jeux et pour faire des recherches scientifiques
mais ils peuvent aussi être utiles dans des applications professionnelles 
(pour générer des clés uniques pour des utilisateurs, des mots de passe, etc.).
Vous allez apprendre comment ils sont générés et en créer vous-même avec une des méthodes les plus simples.

Voici une des premières méthodes pour produire une séquence de nombres qui semblent indépendants (c'est à dire **pseudo-aléatoires**).

1. Choisissez un nombre aléatoire avec 4 chiffres (c'est à dire entre `0000 ... 9999`).
2. Le multiplier par lui-même (c'est à dire le mettre au carré) pour avoir une valeur de 8 chiffres (ajoutez des zéro non-significatifs si besoin).
3. Enlever les 2 premiers chiffres et les 2 derniers chiffres du résultat.
4. La nouvelle valeur contiendra 4 chiffres et sera la prochaine valeur de la séquence.
5. Pour avoir les valeurs suivantes, répétez à partir de l'étape 2.

Exemple

    5761                      - premier nombre de la séquence
	5761 * 5761 = 33189121    - mis au carré
	33(1891)21 => 1891        - tronqué pour avoir les chiffres du milieu
	
	1891                      - deuxième nombre de la séquence
	1891 * 1891 = 3575881     - mis au carré (ajout de zéros non-significatifs pour avoir 8 chiffres)
	03(5758)81 => 5758        - tronqué pour avoir les chiffres du milieu
	
	5758                      - troisième nombre de la séquence (etc.)

Il est évident que tôt ou tard, les séquences arriveront à une sorte de boucle, par exemple :

    0001 -> 0000 -> 0000                   - boucle à la 2ème itération
	4100 -> 8100 -> 6100 -> 2100 -> 4100   - boucle à la 4ème itération
  

Vous allez recevoir les premiers nombres de plusieurs séquences. 
Pour chacune d'entre elles donnez le nombre d'itérations nécessaires pour que la boucle commence.

**Input data** contient sur la première ligne le nombre de valeurs initiales données. 
La deuxième ligne contient les valeurs initiales séparées par des espaces.    
**Answer** doit contenir le nombre d'itérations pour que les séquences arrivent dans une boucle 
avec un espace comme séparation entre les valeurs.

Exemple:

    input data:
	3
	0001 4100 5761
	
	answer
	2 4 88

*Astuce: Pour tronquer la valeur de 8 chiffres, divisez le par `100` et ensuite prenez le reste de la division par `10000`.*
	
