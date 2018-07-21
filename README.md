# [Code Pratique] - Sciences Po'

- Enseignant : Karl Pineau
- Contact : karl.pineau@utc.fr

## Plan du cours :
### Créons notre site web
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
### La partie plus théorique
- Théorie du web
    - Différence entre le web et internet
    - http / https
    - URL, URI
### À vous de jouer
- Créez votre CV


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

#### Qu'est-ce que le HTML ?
Le HTML est un **langage de programmation**. C'est un acronyme qui signifie *HyperText Markup Language*, autrement dit un 
langage permettant de marquer de l'hypertexte.

#### Qu'est-ce que de l'hypertexte ?
L'hypertexte est la notion centrale du Web inventé à la fin des années 80 par Tim Berners-Lee. L'hypertexte est une notion
qui préexiste au Web, mais que le web exploite dans toute sa puissance.

C'est tout simplement l'idée de placer un lien dans une zone de texte à l'intérieur d'un document amenant à un autre document.

![Les liens hypertexte, source Wikimédia](https://upload.wikimedia.org/wikipedia/commons/4/41/Sistema_hipertextual.jpg)

Depuis l'invention du HTML, on lui a trouvé de nombreux autres objets sémantiques représentables : des titres, des paragraphes,
des images, des tableaux. On exprime donc en HTML bien plus de choses que seulement des liens.

#### Matérialiser le HTML : la notion de balise
Pour indiquer au navigateur parcourant votre fichier HTML où se trouvent les éléments signifiants (par exemple un titre),
on utilise une ou plusieurs balises qui vont venir encadrer le texte que vous souhaitez marquer.

**Revenez à votre fichier bonjour.html**
1. Complétons un peu le fichier pour commencer. Sautez une ligne et inscrivez *"What's up?"*
2. Sauvegardez votre fichier, retournez sur votre navigateur et raffraichissez votre page. Votre site a évolué :)

À présent, ajoutons une première brique HTML à notre fichier :
1. Sur la première ligne, qui contient *"Hello, World!"*, ajoutez la balise `<h1>` devant votre phrase et la balise `</h1>` 
derrière.
2. Vous obtenez le code suivant :

    `<h1>Hello, World!</h1>
    What's up?`

3. Sauvegardez votre fichier, retournez sur votre navigateur et raffraichissez votre page.