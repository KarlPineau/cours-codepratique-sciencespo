**[Cours de Code Pratique](../README.md)**
# À la découverte de la programmation web

## Premiers pas
1. Ouvrir un éditeur de texte simple (textEdit sur Mac)
2. Y écrire `Hello, World!`
3. L'enregistrez-sous sur le bureau & l'intituler **bonjour.html**
4. Ouvrir le fichier depuis le bureau avec un navigateur (double-cliquer dessus simplement)
5. Voici votre premier site web :)

#### Ce mini-site est-il en ligne ?
Deux formats d'URL :
- `file:///Users/karlpineau/Desktop/bonjour.html`
- `https://fr.wikipedia.org/wiki/Wikipédia:Accueil_principal`

#### Matérialiser le HTML : la notion de balise
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
balise `<h1>` et ne pas écrire sa balise `</h1>` ensuite :
    - Faisons le test : **supprimez la balise `</h1>`** de votre fichier **bonjour.html** ;
    - Sauvegardez votre fichier, retournez sur votre navigateur et raffraichissez votre page ;
    - Le navigateur doit interpréter tout votre texte comme étant le titre ;
    - Sur certains navigateur (comme Firefox), si vous faites un clic droit sur votre page puis "Afficher le code source",
    le navigateur vous affiche en rouge les balises non correctes ;
    - Remettons notre balise `</h1>` en place.
- Vous **ne pouvez pas non plus entremêler les balises**. Ainsi `<p><a></a></p>` est valide car la balise `p` contient la balise `a`. Par contre, `<p><a></p></a>` n'est pas valide car la notion d'arborescence n'est pas respectée ;
- Il est **très important** de comprendre que si votre navigateur a modifié le style (l'apparence visuelle) de votre titre
lorsque vous lui avez indiqué qu'il s'agissait d'un titre, **vous ne lui avez pour autant indiqué aucune consigne d'ordre visuel**.
L'action de pose de la balise `<h1>` est une action **sémantique**. Vous avez donné du sens à votre texte. Votre navigateur 
en a déduit seul une apparence visuelle. 


**[Partie suivante](../installation-ide/README.md)**
