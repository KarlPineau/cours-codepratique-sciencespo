**[Cours de Code Pratique](../README.md) | [Partie précédente](README.md)**

# La mission Dakar-Djibouti : mise en forme

## Créons notre fichier CSS
- Ouvrez un nouveau fichier sur Atom.io ;
- Inscrivez-y `img {max-width: 300px;}` ;
- Enregistrez-le sous le nom de `style.css` ;
- Dans le fichier index.html, ajoutez la ligne suivante à votre head : `<link rel="stylesheet" href="style.css" type="text/css" />`

## Installer une police d'écriture :
- Liste des polices installées par défaut : https://www.w3schools.com/cssref/css_websafe_fonts.asp
- Polices proposées par Google : https://fonts.google.com/, nous allons utilise **Source Sans Pro** pour nos titre
- Intégrer une police de Google sur votre site : 
  - Copier-coller le code donné par Select this font > Embed > Standard dans le `head` de votre fichier `index.html`, par exemple `<link href="https://fonts.googleapis.com/css?family=Source+Sans+Pro" rel="stylesheet">`
  - Pour utiliser la police, le code est donné par Google, ici : `font-family: 'Source Sans Pro', sans-serif;`
  - Dans notre fichier `style.css` : `h1 {font-family: 'Source Sans Pro', sans-serif;}`

## Appliquer une règle à plusieurs balises :
Pour cela, il suffit de séparer les balises par une virgule devant la règle :

    h1, h2, h3, h4, h5, h6 {
      font-family: 'Source Sans Pro', sans-serif;
    }

## Les tailles de police : 
À vous de jouer !

La taille de police s'exprime par la propriété `font-size`

## Mettre en forme nos paragraphes :
À vous de jouer !

- Appliquer la police de caractère Raleway à tous les paragraphes : https://fonts.google.com/specimen/Raleway
- Appliquer une taille de caractère de 24px à tous les paragraphes

## Comprendre l'héritage :
- Modifions notre dernière règle en :

      body {
        font-family: 'Raleway', sans-serif;
        font-size: 24px;
      }
      
## Cibler un élément spécifique :
- Ajoutons un attribut identifiant à notre image de carte géographique :

      <img id="header-map" src="media/map.jpg" alt="Carte du parcours de l'expédition Dakar-Djibouti" />
      
- Ciblons cet attribut pour notre règle CSS par l'utilisation d'un `#header-map` (le # marque l'attribut id) :

      #header-map {
        max-width: 100%;
      }
      
## Les éléments HTML abstraits :
- Les balises abstraites :
  - `div` pour les balises block (qui génèrent un retour à la ligne avant et après) ;
  - `span` pour les balises inline (qui s'intègrent dans un block)
- Notre `div` à l'intérieur du `header` :

      <header>
          <div>
              <h1>La mission Dakar-Djibouti</h1>

              <p>Entre 1931 et 1933, Marcel Griaule et 9 autres expéditionnaires parcourent l'Afrique d'Ouest en Est avec l'appui de <a href="https://fr.wikipedia.org/wiki/Georges_Henri_Rivi%C3%A8re">Georges Henri Rivière</a>.</p>
              <img id="header-map" src="media/map.jpg" alt="Carte du parcours de l'expédition Dakar-Djibouti" />
          </div>
          <nav>
              <ul>
                  <li><a href="#contexte">Contexte de l'expédition</a></li>
                  <li><a href="#membres">Les membres de l'expédition</a></li>
                  <li><a href="#parcours">Le parcours de l'expédition</a></li>
                  <li><a href="#objets">Des objets de l'expédition</a></li>
                  <li><a href="#galerie">Galerie de photos</a></li>
                  <li><a href="#sons">Ecoutons les sons de l'expédition</a></li>
                  <li><a href="#sources">Sources de cette page</a></li>
              </ul>
          </nav>
      </header>

## Les classes :
- Appliquons la classe à notre `div` :

      <div class="center">
          <h1>La mission Dakar-Djibouti</h1>
          
- Puis, dans notre fichier `style.css` (en remplacement de `header {text-align : center};`):

      .center {
        text-align: center;
      }

## Appliquer une bordure à notre citation :
- Pour obtenir une bordure de 10px d'épaisseur, en trait plein, de couleur grise :
  
      blockquote {
        border: 10px solid #CCCCCC;
      }
      
- Pour n'afficher la bordure que sur le côté gauche, modifions `border` en `border-left` :

      blockquote {
        border-left: 10px solid #CCCCCC;
      }    
      
- Enfin, pour que la bordure ne soit pas collée au texte, utilisons la propriété espacement interne, `padding` :

      blockquote {
        border-left: 10px solid #CCCCCC;
        padding: 10px;
      }
      
## Les couleurs en CSS :
- On matérialise les couleurs par un code hexadécimal : de #000000 (tout noir) à #ffffff (tout blanc)
- Utiliser http://www.color-hex.com/ pour obtenir des codes depuis une couleur

## Faire flotter un élément :
- Créez une classe `float-right` pour notre image de l'équipe
- Créez la règle CSS suivante :

      .float-right {
        float: right;
      }
      
- Plaçons l'image avant la liste : 

      <section id="membres">
            <h2>Les membres de l'expédition</h2>

            <img class="float-right" src="media/membres.jpg" alt="Les membres de l'expédition Dakar-Djibouti avant le départ" />
            <ul>
                <li><a href="https://fr.wikipedia.org/wiki/Andr%C3%A9_Schaeffner">André Schaeffner</a>, anthropologue, ethnomusicologue</li>
                <li><a href="https://en.wikipedia.org/wiki/Deborah_Lifchitz">Deborah Lifchitz</a>, linguiste</li>
                <li><a href="https://fr.wikipedia.org/wiki/Michel_Leiris">Michel Leiris</a>, écrivain, ethnologue</li>
                <li><a href="https://fr.wikipedia.org/wiki/Marcel_Griaule">Marcel Griaule</a>, ethnologue</li>
                <li><a href="https://fr.wikipedia.org/wiki/%C3%89ric_Lutten">Éric Lutten</a>, ethnologue</li>
                <li><a href="https://fr.wikipedia.org/wiki/Jean_Mouchet">Jean Mouchet</a>, linguiste, ethnologue</li>
                <li><a href="https://fr.wikipedia.org/wiki/Gaston-Louis_Roux">Gaston-Louis Roux</a>, dessinateur & peintre</li>
                <li>Abba Jérôme Gabra Mussié, lettré éthiopien, interprête</li>
                <li>Marcel Larget, naturaliste</li>
                <li>Abel Faivre, géographe et naturaliste</li>
            </ul>

        </section>

## Rendre la taille des images relatives :
On passe de :

    img {
      max-width: 300px;
    }
    
À :

    img {
      max-width: 40%;
    }

## Mettre en forme notre tableau :
- Pour obtenir un tableau centrée :

      table {
        margin-left: auto;
        margin-right: auto;
      }
      
- À vous de faire l'espacement en s'aidant pour la propriété `padding` des spécifications `left`, `top`, `right` et `bottom` pour obtenir une marge de 10px en haut et en bas, et de 20px sur les côtés.

- Enfin pour colorer une ligne sur deux :

      tr:nth-child(even) {
        background-color: #f2f2f2;
      }
      
Nous obtenons à la fin :
    
    table {
      margin-left: auto;
      margin-right: auto;
    }
    th {
        background-color: #444444;
        color: white;
    }
    th, td {
        padding: 10px 20px;
    }
    tr:nth-child(even) {
      background-color: #f2f2f2;
    }

## Les objets :
À vous d'agencer le code HTML, voici la partie CSS :

    .object-article {
        vertical-align: top;
        max-width: 23%;
        display: inline-block;

        margin: 5px;

        border: 3px solid #CCCCCC;
        border-radius: 5px;
    }

    .object-img {
        max-width: 100%;
        border-top-left-radius: 4px;
        border-top-right-radius: 4px;
    }

    .object-h3, .object-p {
        margin: 10px;
    }

    .object-p {
      font-size: 90%;
    }
    
## Les photos :
À vous de reproduire la même structure pour les photos.

## C'est la fin
Vous avez désormais un site relativement mis en page. Le code complet [est disponible ici](https://github.com/KarlPineau/cours-codepratique-sciencespo/tree/master/mission-dakar-djibouti).

**[Partie suivante](../curriculum-vitae/README.md)**
