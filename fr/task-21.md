Sur ce problème, vous allez apprendre une astuce de programmation populaire utilisable de 
plusieurs façons pour effectuer des calculs ou des statistiques.  

Imaginez qu'un bûcheron essaie de compter les pins, les sapins et les bouleaux sur une partie de la forêt. 
Il peut traverser cette partie 3 fois en comptant les pins au premier tour, les sapins au deuxième tour puis les bouleaux au troisième tour.

Une manière plus efficace serait qu'il ne fasse qu'un seul passage à travers la forêt et pour chaque arbre ajouter, sur son carnet, un point sur une page dédiée à chaque type d'arbre, la première page pour les pins, la deuxième pour les sapins 
et la dernière pour les bouleaux. L'idée est de compter ces éléments similaires en utilisant un tableau de compteurs (à la place d'un carnet).
  
Voici un tableau de longueur `M` contenant des nombres de `1 ... N`, où `N` est plus petit ou égal à `20`.  
Vous devez le parcourir et compter le nombre de fois où chaque nombre apparait. 
C'est comme le problème [Vowel Count](./vowel-count), mais il faut garder plus d'un compteur en mémoire.  
Utilisez bien un tableau pour les compteurs et de ne pas créer de variable pour chaque compteur.  

**Input data** contient les valeurs `M` et `N` sur la première ligne.  
La deuxième ligne (plutôt longue) contiendra `M` nombres avec un espace comme séparation entre les valeurs.  
**Answer** devra contenir exactement `N` valeurs, avec un espace entre chaque réponse. 
La première valeur donnera le nombre de `1`, la deuxième le nombre de `2`, etc.

Exemple:

	data input:
	10 3
	3 2 1 2 3 1 1 1 1 3
	
	answer:
	5 2 3
