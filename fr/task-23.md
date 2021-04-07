Ce problème est un exercice pour apprendre le principe du célèbre algorithme de classement le [bubble sort](./bubble-sort) 
que vous pourrez voir plus tard.

En partant d'un tableau de nombres, il faut parcourir toutes les paires de nombres voisins dans l'ordre, 
puis d'échanger les nombres des paires où le premier nombre est plus grand que le deuxième.

Par exemple, voici un tableau de nombres simple, `1 4 3 2 6 5` et ci-dessous quelles paires doivent être permutées ou pas pour un passage.

	(1  4) 3  2  6  5  - passe
	1 (4  3) 2  6  5  - permute
	1  3 (4  2) 6  5  - permute
	1  3  2 (4  6) 5  - passe
	1  3  2  4 (6  5) - permute
	1  3  2  4  5  6  - fin
  
Cette opération déplace les nombres les plus grands vers la droite (fin du tableau) et les plus petits vers la gauche (début du tableau).  
Le plus important est que **le nombre le plus grand est obligatoirement amené à la fin du tableau**.


**Input data** contient tous les nombres du tableau, ils sont tous positifs. 
Le nombre `-1` montre la fin du tableau (il ne fait pas partie du tableau).  
**Answer** doit contenir 2 valeurs : le nombre de permutations faites et la somme de contrôle du tableau trié, avec un espace comme séparation entre les valeurs.  
La somme de contrôle doit être calculée de la même façon que dans l'exercice [Array Checksum](./array-checksum).

Exemple:

	input data:
	1 4 3 2 6 5 -1
	
	answer:
	3 5242536
