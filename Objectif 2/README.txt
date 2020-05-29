On a changé notre librairie par gfssp72 pour cet objectif. 

Notre programme renvoie un tableau de 6 valeurs (qui reprèsente les 6 joueurs et donc les 6 fréquences des 6 pistolets), chaque fois qu'on signal est capté, on fait le calcul de la DFT
et on incrémente la valeur du tableau qui correspond à la fréquence du pistolet capté (il s'agit de son score).
Pour tester, on ouvre la fenêtre "logic analyzer" du débug, on va dans "setup" et on rentre les 6 compteurs un à un en validant à chaque compteur (compteurs[0], compteurs[1], ... , compteurs[6])
Pour chaque compteur on met la range max : 30 et min : 0. Ensuite on exécute, on attends un peu (30 secondes) pour que chaque signaux soient envoyé et on observe le résultat.

On a rajouté un tableau score de 6 éléments (à mettre en plus dans le setup de la logic analyser (score[0], score[1], ... score[5] avec une range max : 6 min : 0) pour visualiser le score de chaque joueur.
La variable "passe" permet de ne passer qu'une fois dans la boucle d'incrémentation du score pour éviter que ça y retourne sur toute la plage. 

Objectif fini et fonctionnel.