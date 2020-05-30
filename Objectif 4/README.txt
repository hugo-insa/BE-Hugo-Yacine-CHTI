Dans cette partie nous avons rassemblé toutes les parties précédentes pour arriver au jeu final. Au terme de cette partie, on observe les scores de tous
les joueurs qui évolue en fonction de si le signal du pistolet a été capté, de même le son se lance à chaque signal de pistolet.
Nous avons réalisé le programme avec le signal 0x33 on attend donc 1 tir  a  85kHz (k=17)     2 tirs a  90kHz (k=18)     3 tirs a  95kHz (k=19)     4 tirs a 100kHz (k=20)     5 tirs a 115kHz (k=23)

Pour les tests
Dans les setup de la logic analyzer on rajoute les variables suivantes :
compteurs[0] à compteurs[5] avec une range max 30 min 0
score[0] à score[5] avec une range max 6 et min 0
TIM3_CCR3 avec une range max 360 et min 0

Les compteurs indique à chaque fois qu'on capte un signal d'une certaine fréquence (compteurs[0] = 85kHZ, compteurs[1] = 90kHZ etc...).
Les score indique le nombre de fois qu'on a capté un signal pour chaque fréquence (score[0] = 85kHZ, score[1] = 90kHZ etc...).
TIM3_CCR3 permet de bien voir qu'on envoie un bruit de pistolet a chaque fois qu'on capte un signal. 

Objectif final atteint et fonctionnel. 