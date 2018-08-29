**[Cours de Code Pratique](../README.md) | [Partie précédente](../javascript/README.md)**

# Sauvegarde, collaboration, mise en ligne :

## Sauvegarder sur GitHub :
- GitHub (le site sur lequel vous vous trouvez en ce moment) : https://github.com
- Git (le logiciel pour faire fonctionner Github) : https://git-scm.com/
- Ajouter un projet à GitHub :
    - Ouvrir le terminal de votre ordinateur :

            cd /Sites/mon-site
            git init
            git remote add origin [url de votre repository]
            git add *
            git commit -m “Mon premier commit”
            git push -u origin master
     

- Plus d'information sur l'envoi de fichiers sur GitHub : https://guides.github.com/activities/hello-world/


## Mettre en ligne un site :
- Pages : https://pages.github.com/
- OVH : https://www.ovh.com/fr/

## Essayons de mettre en ligne notre site :
- Pour mettre en ligne votre site web, il faut utiliser un logiciel de FTP : https://filezilla-project.org/
- Une fois que vous l'avez lancé, il y a une barre de connexion rapide en haut, dans laquelle il faut remplir les valeurs suivantes :
    - Hôte : ftp.karl-pineau.fr 
    - Identifiant : karlpine-sciencespo
    - Mot de passe : SciencesPo2018
- Créez dans la zone de droite un dossier à votre nom, en utilisant des tirets pour remplacer les espaces ;
- Naviguez dans la zone de gauche à l’endroit de votre ordinateur où se trouve votre CV en site web ;
- Sélectionnez les fichiers de votre site sur votre ordinateur, cliquez droit et choisissez “Envoyer” ;
- Allez à l’adresse : http://sciencespo.karl-pineau.fr/votre-nom ;
