**[Cours de Code Pratique](../README.md) | [Partie précédente](README.md)**

# La mission Dakar-Djibouti : mise en forme

## Créons notre fichier CSS
- Ouvrez un nouveau fichier sur Atom.io ;
- Inscrivez-y `img {max-width: 300px;}` ;
- Enregistrez-le sous le nom de `style.css` ;
- Dans le fichier index.html, ajoutez la ligne suivante à votre head : `<link rel="stylesheet" href="style.css" type="text/css" />`

## Installer une police d'écriture :
- Liste des polices installées par défaut : https://www.w3schools.com/cssref/css_websafe_fonts.asp
- Polices proposées par Google : https://fonts.google.com/
- Intégrer une police de Google sur votre site : 
  - Copier-coller le code donné par Select this font > Embed > Standard dans le `head` de votre fichier `index.html`, par exemple `<link href="https://fonts.googleapis.com/css?family=Source+Sans+Pro" rel="stylesheet">`
  - Pour utiliser la police, le code est donné par Google, ici : `font-family: 'Source Sans Pro', sans-serif;`
  - Dans notre fichier `style.css` : `h1 {font-family: 'Source Sans Pro', sans-serif;}`

## Appliquer une règle à plusieurs balises :
Pour cela, il suffit de séparer les balises par une virgule devant la règle :

    h1, h2, h3, h4, h5, h6 {
      font-family: 'Source Sans Pro', sans-serif;
    }
