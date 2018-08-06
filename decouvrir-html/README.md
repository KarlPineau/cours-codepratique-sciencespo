**[Cours de Code Pratique](../README.md)**
# À la découverte de la programmation web

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

    `<h1>Hello, World!</h1>`    
    `What's up?`

3. Sauvegardez votre fichier, retournez sur votre navigateur et raffraichissez votre page.

Vous constatez que votre ligne *"Hello, World!"* est devenue nettement plus visible. C'est normal, votre navigateur vient 
d'interpréter votre code.

#### Comprendre ce qu'il vient de se passer :
- La balise `h1` est utilisée en HTML pour indiquer un titre de premier niveau (c'est l'abréviation de *heading 1*). 
Le titre de premier niveau est le titre principale d'un document ;
- On a donc placé deux balises, une balise **ouvrante** (`<h1>`) qui indique où commence notre titre et une balise 
**fermante** (`</h1>`) qui indique où s'arrête notre titre ;
- Chaque balise commence par un symbole **<** (chevron ouvrant, strictement plus petit que) et se finit par un symbole **>** 
(chevron fermant, strictement plus grand que) ;
- Le texte à l'intérieur de la balise indique le type de la balise : `<h1>` est une balise `h1`, `<p>` est une balise `p`
- La balise **fermante** possède un slash **/** juste après le chevron ouvrant ;
- Les **balises fonctionnent toujours par couple** (ou presque, on verra ça plus loin). Vous ne pouvez pas écrire une 
balise `<h1>` et ne pas écrire sa balise `</h1>` ensuite
    - Faisons le test : **supprimez la balise `</h1>`** de votre fichier **bonjour.html** ;
    - Sauvegardez votre fichier, retournez sur votre navigateur et raffraichissez votre page ;
    - Le navigateur doit interpréter tout votre texte comme étant le titre.
    - Sur certains navigateur (comme Firefox), si vous faites un clic droit sur votre page puis "Afficher le code source",
    le navigateur vous affiche en rouge les balises non correctes.
    - Remettons notre balise `</h1>` en place.
- Il est **très important** de comprendre que; si votre navigateur a modifié le style (l'apparence visuelle) de votre titre
lorsque vous lui avez indiqué qu'il s'agissait d'un titre, **vous ne lui avez pour autant indiqué aucune consigne d'ordre visuel**.
L'action de pose de la balise `<h1>` est une action **sémantique**. Vous avez donné du sens à votre texte. Votre navigateur 
en a déduit seul une apparence visuelle. 