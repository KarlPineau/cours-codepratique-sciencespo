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
          
- Puis, dans notre fichier `style.css` (en remplacement de `header {text-align : center};`:

      .center {
        text-align: center;
      }

