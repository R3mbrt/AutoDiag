AutoDiag


Ceci est un repos pour la création et le développement d'un système de diagnostic automatisé pour les ordinateurs.

Etant technicien en SAV dans une des entreprises en tant que leaders du e-commerce high-tech, on tombe parfois sur des diagnostics assez ouf, donc si je pouvais trouver un moyen d'automatiser l'ensemble des tests, gains de temps, ça tourne la nuit et montage de PC à gogo !!


Actuellement, je fais ceci pour moi et moi seul. Si une personne souhaite me partager des connaissances, infos ou amélioration, je suis preneur, mais étant actuellement au début du projet, je vais déjà commencer par me péter le crâne sur la table en solo et comprendre mes erreurs.


## Table of Contents

  * [Le but du projet](#Le-but-du-projet)
  * [Les test](#Les-test)


	## Le but du projet

		1 - Le plan : créer un éco-système permettant le boot de différents outils via un système PXE, ventoy ou maison (par la création d'un équivalent). Il faut un bouton pour faire tous les tests de façon automatique avec push du résultat et la possibilité de lancer un test seul (RAM, HDD etc.)
		2 - Il nous faut d'en un premier temps commencé par faire boot un test mémoire, l'avantage, c'est que du code complet est déjà dispo, on va donc pouvoir se reposer la dessus. L'ensemble devrait reposer sur GRUB.
		3 - Une fois notre test mémoire "Pass" or "Failed" il va falloir inscrire le résultat sur un serveur (NFS de préférence, voir des infos sur le PXE et ses bien-faits) --> push du résultat.
		4 - Un boot sur un équivalent de hdck ou whdd en version libre (pssst, tu viens déjà de boot un noyau unix avec ton memtest, tu peux t'en servir à nouveau pour la suite ?) --> push du résultat.
		5 - Stresstest de la machine composant après composant et test de l'ensemble (test de chauffe, erreur de calcul, de rendu, VRAM, 3D, cuda et opencl etc.) bref, on passe au peigne fin tout ça.
		6 - Si on est sur un laptop, on chck la batterie (dans la mesure du possible bien sûr, en gros : cellule HS ? Usure importante ? Autonomie? etc.)
		7 - On affiche la version du BIOS (si possible faire une concordance avec les sites constructeurs pour récupérer le numéro de la dernière version)

	## Les test
		Pour le moment, tout sera fait avec une VMs, un vieux laptop avec un core de 6eme gen, un macbook pro a1218 et un T480.
	    Le projet sera dev sur visual studio 2022, VS code et un Ubuntu des familles.


RELEASE :
		v0.01 08-06-2023 _ Push du README et mise en place du repos en public + création de branche privé
