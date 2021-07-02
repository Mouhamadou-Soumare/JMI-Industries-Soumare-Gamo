Projet PWEB Symfony 5.1 Christian GAMO Mouhamadou SOUMARE Groupe 206

Mail en cas de besoin : christian.gamo.pro@gmail.com

Base de données : 
Utilisateur [id, nom, mdp, email, isLoueur]
Vehicule [id, type, caract, location, image, prix_jour]
Facturation [id, ide, idv, dateD, dateF, valeur, etat]


Pour lancer notre projet, il faut aller sur le terminal en mode admin et utiliser la commande cd 
pour se placer dans le répertoire contenant notre projet.

Ensuite il faut lancer les commandes :

//pour lancer le serveur
$>symfony serve -d 

//pour créer la base mySQL stocké chez l'user root avec mot de passe root
//vérifier le .env pour choisir la base à la ligne :
//DATABASE_URL=mysql://root:root@127.0.0.1:3306/projetPWEB_GAMO_SOUMARE_206?serverVersion=5.7
//root:root étant du format user:mdp          			
$>php bin/console doctrine:database:create	

/créer les tables							
$>php bin/console make:migration
$>php bin/console doctrine:migrations:migrate

//mettre en place le jeu de données dans la base
$>php bin/console doctrine:fixtures:load
	

Comptes dans le jeu de données:

Compte administrateur:

email : sense@gmail.com
mdp : sense1234


Compte loueur:

email : ilie@gmail.com
mdp : ilie1234


Comptes client:

email : christian@gmail.com
mdp : christian1234

email : mouhamadou@gmail.com
mdp : mouhamadou1234

email : polnareff@gmail.com
mdp : polnareff1234
