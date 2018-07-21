# [Code Pratique] - Sciences Po'

- Enseignant : Karl Pineau
- Contact : karl.pineau@utc.fr

## Plan du cours :
### Matin : créons notre site web
- Choix d'un thème de découverte :
    - La mission Dakar - Djibouti (culture, ethnographie)
    - Un sujet de politique internationale
    - Un sujet de sport ?
- Premières balises HTML
- Contenu de la page
- Structure de la page
- Mettons en forme
- Animons
- Mettre en ligne
### Après-midi : la partie plus théorique
- Théorie du web
    - Différence entre le web et internet
    - http / https
    - URL, URI


## Introduction
- Qui a déjà fait de la programmation auparavant ?
- Intérêt d'apprendre les bases en programmation, notamment web

## Premiers pas
1. Ouvrez un éditeur de texte très simple (textEdit sur Mac)
2. Tapez-y *"Hello, World!"*
3. Enregistrez-sous votre fichier sur votre bureau, intitulez-le **bonjour.html**
4. Rendez-vous sur votre bureau, ouvrez-votre fichier avec votre navigateur préféré (double-cliquez dessus simplement)
5. Voici votre premier site web :)

### Comprendre ce qui a été fait :
En enregistrant votre fichier sous un format spécifique (.html), vous avez indiqué à votre ordinateur qu'il s'agissait 
d'un fichier utilisé pour un site web. Votre ordinateur l'a donc transmis à votre navigateur web, qui l'a interprété en 
tant que site web.

#### Ce mini-site est-il en ligne ?
Non, pour l'instant, ce site n'existe que sur votre ordinateur. Il évolue dans votre **environnement local**, aussi appelé
**localhost**.

En regardant l'URL qui s'affiche sur votre navigateur, vous constaterez qu'elle pointe à l'intérieur de votre ordinateur, 
et non sur une adresse web. L'URL affichée doit ressembler à quelque chose du type :

    file:///Users/karlpineau/Desktop/bonjour.html

Alors qu'une adresse web, ça serait :

    https://fr.wikipedia.org/wiki/Wikipédia:Accueil_principal

Vous noterez ici deux différences majeures :
- Sur votre ordinateur, vous n'avez pas de **nom de domaine**, n'est indiquée dans votre URL que la liste des dossiers 
que vous parcourez. Sur un site web, vous trouvez dans la deuxième partie de votre URL un nom de domaine qui explicite 
le site sur lequel vous vous trouvez, dans notre exemple `fr.wikipedia.org`. Ce n'est donc qu'après cela que vous trouvez 
dans l'URL les fichiers et dossiers qui composent l'arborescence du site dans laquelle vous naviguez. 
- Le protocole utilisé : `file:` indique que l'on navigue dans les fichiers de votre ordinateur. Alors que sur le web, 
on utilise le protocole `http:`
    
Nous travaillerons à mettre votre site web en ligne plus tard :)
