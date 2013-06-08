Orleans - R Clustering scripts
==============================


Les scripts principaux sont :

	- main-install.R: 	installe les librairies R n�cessaire � l'ex�cution 
						des scripts (� ex�cuter une seule fois). 
					
	- main-generation.R:	�crit pour g�n�rer des donn�es bidons, afin de tester 
							les autres scripts.
			- data.txt:	fichier g�n�r�, contenant les donn�es brutes. les donn�es 
						r�elles doivent respecter ce format tabulaire.
			- data.pdf: repr�sentation graphique des donn�es. une ACP est r�alis�e 
						pour extraire seulement les deux vecteurs principaux.
			- pca.txt:	r�sultats de l'ACP, cach�s pour �tre r�utilis�s plus tard 
						si n�cessaire. 
									
	- main-process.R:	applique les algorithmes de clustering, puis les compare.
						certains r�sultats sont cach�s dans des fichiers:
			- distances.bin:	objet R repr�sentant la matrice de distances.
			- ALGO.txt: 		vecteur d'appartenance g�n�r� par l'algorithme de 
								clustering <ALGO>. Chaque valeur correspond au 
								num�ro de cluster d'une instance.
			- performances.txt:	table contenant la valeur de Silhouete maximale 
								obtenue pour chaque algo de clustering, ainsi que 
								le nombre de clusters d�tect�s.
			- ari.txt:			matrice comparant les clusters de chaque algo 2 � 
								2, en utilisant l'index de Rand ajust� (ARI).

Le reste des fichiers contient des fonctions utilis�es par ces scripts.
