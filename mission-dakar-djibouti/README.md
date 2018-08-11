# Exemple de page web : la Mission Dakar-Djibouti

## Mettre en place notre environnement de travail
- Où se positionner sur votre ordinateur :
  - Sur Mac, rendez-vous dans le dossier `Sites` (depuis votre dossier home). Il se peut que ce dossier n'existe pas encore, auquel cas, vous pouvez l'y créer (depuis home).
  - Sur Windows, créez un dossier `Sites` où vous voulez
- Créez un sous dossier `mission-dakar-djibouti`
- Récupérez [le dossier de contenus sur GitHub](media) et copiez-collez le contenu dans votre dossier

## Créons la page d'accueil de notre site
- Lancez le logiciel **Atom.io** (un nouveau fichier s’ouvre automatiquement)
- Ecrivez dans votre fichier `Découvrez la mission Dakar-Djibouti`
- Sauvegardez-sous votre fichier, placez-le dans votre dossier `mission-dakar-djibouti` et intitulez-le `index.html`

## Construire la structure initiale de notre site web
- Supprimez ce qui pré-existe comme texte dans la page
- Inscrivez :

      <!DOCTYPE html>
      <html>
      
      </html>
      
- À l'intérieur de `<html></html>`, plaçons nos balises `<head></head>` et `<body></body>`

      <head>
      
      </head>
      <body>
          Découvrez la mission Dakar-Djibouti
      </body>

## Remplissions notre `<head>` :
À l'intérieur de `<head></head>`, plaçons une balise `<title>` pour donner un titre à notre page et une balise `<meta>` pour indiquer un encodage à appliquer :

      <title>Découvrez la mission Dakar-Djibouti</title>
      <meta charset="utf-8">
      
## Utiliser les attributs :
À l'intérieur de notre `body`, plaçons notre titre dans une balise de premier niveau :

      <body>
        <h1>Découvrez la mission Dakar-Djibouti</h1>
      </body>
      
Puis ajoutons l'attribut `title` à notre balise `h1`:
 
      <h1 title="Ce texte s'affiche au survol">Découvrez la mission Dakar-Djibouti</h1>

## Présentation du résultat final

## Allons-y
