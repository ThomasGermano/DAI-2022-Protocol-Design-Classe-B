___
## Objectifs:
créer une calculatrice avec diverses fonction de calculs. Il y aura un coté 
server qui va recevoir les arguments du client et effectuer le calcul. Le server va 
envoyer la réponse du calcule au client qui va l'afficher. 
___
## Comportement:
-On utilise le protocol TCP port 80, localhost.  
-le client parle en premier.  
-Client ferme la connection et server aussi apres un countdown. 
___
## Messages:
quand connection: affiche la co du client -> ready state  
ensuite en attente...
client lance le calcule avec syntaxe : nb opérande nb ex:(2 * 8)  
server repond: 2 * 8 = 16  
si autre connection server multithread donc répéte msgs d'accueil..  
___
## Elements spécifique:
supporte addition et multi, si autre lance du erreur et invite la personne a 
resaisir.
___
## Exemple:
client: syn  
server: syn-ack  
client: ack  
server: please enter calcul..  
client: 2 * 8  
server: 2 * 8 = 16  
server: new calcul please or send bye..  








