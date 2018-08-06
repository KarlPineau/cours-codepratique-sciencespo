**[Cours de Code Pratique](../README.md) | [Partie précédente](../curriculum-vitae/README.md)**

# Rendons notre site interactif avec JavaScript :

## Vue.js, une bibliothèque simple à prendre en main :
- Documentation de Vue.js : https://vuejs.org/v2/guide/
- Commençons un nouveau fichier `mon-site-javascript.html`, au sein duquel on place un appel à la bibliothèque Vue.js :

        
        <!DOCTYPE html>
        <html lang="en">
        <head>
            <meta charset="UTF-8">
            <title>Title</title>
        </head>
        <body>
        
            <script src="https://cdn.jsdelivr.net/npm/vue/dist/vue.js"></script>
        </body>
        </html>
        
- Ajoutons ensuite, dans le haut du `<body>` :


        <div id="app">
          {{ message }}
        </div>
        

- Puis, sous l'appel à Vue.js :


        <!-- Placer cette partie SOUS l'appel à la library Vue.js -->
        <script>
            var app = new Vue({
              el: '#app',
              data: {
                message: 'Hello Vue!'
              }
            })
        </script>
        
- Sauvegardez & admirer le résultat
        
## Partons à la découverte des APIs:
- Pour obtenir la météo de Paris | [API OpenWeatherMap](http://openweathermap.org) : `http://api.openweathermap.org/data/2.5/weather?q=Paris,fr&APPID=6586e6c52e104e0929ebeeb07d5f2c55&units=metric` (attention, sur cette URL, le nombre de requêtes est limité à 60 par minute. Ne pas trop cliquer)
- Pour obtenir une carte de Paris | [API Google Maps](https://www.google.com/maps/) : `https://www.google.com/maps/search/?api=1&query=Paris`
- Pour obtenir des informations sur Paris | [API Geonames](http://geonames.org) : `http://api.geonames.org/getJSON?formatted=true&geonameId=2988507&lang=fr&username=demo&style=full`


## Une application pour la météo
Nous allons donc construire une petite application demandant la météo. Pour cela, nous allons utiliser les services 
d'OpenWeatherMap, via leur API.

- Commençons par ajouter sous notre appel à la library Vue.js celui à l'appel la library Axios.js
        
        
        <script src="https://unpkg.com/axios/dist/axios.min.js"></script>
        
- Pour demander à l'utilisateur d'indiquer la ville dont il souhaite voir la météo, nous allons utiliser un formulaire,
avec un champ de saisie et un bouton de validation. Ajoutons au-dessous une balise `pre` dont le rôle est d'afficher un résultat
 de code sous forme textuel, qui affichera le résultat de la météo :

        
        <form method="get" action="#">
            <label for="city">Pour quelle ville souhaitez-vous la météo ?</label>
            <input id="city" v-model="city">
            <button @click="getContent(city)">Retrieve</button>
        </form>
        <pre>{{ weather }}</pre>
        
- Nous allons ensuite générer notre instance de Vue.js :


        var app = new Vue({
            el: '#app',
            data: {
                city: '',
                weather: 'Pas de météo pour le moment'
            },
            methods: {
                getContent: function(city) {
                    return axios.get("http://api.openweathermap.org/data/2.5/weather?q="+city+"&APPID=6586e6c52e104e0929ebeeb07d5f2c55&units=metric")
                        .then(response => {this.weather = response.data;})
                }
            }
        });
        
- Nous déclarons donc ici un ensemble de données :
    - La valeur `city` correspond au champ de notre formulaire
    - La valeur `weather` est ce que OpenWeatherMap nous retourne
    
- Nous définissons ensuite une méthode `getContent` dont le rôle est de soumettre notre requête à OpenWeatherMap et de nous retourner le résultat

- Sauvegardons et rechargeons la page

- Admirez le résultat

### Mettons un peu de mise en forme sur notre météo
Vous le constatez, le rendu n'est pas vraiment lisible... Nous allons donc remplacer `<pre>{{ weather }}</pre>` par :

        <div v-if="weather !== null">
            <h2>Voici la météo de {{ weather['name'] }}</h2>

            <dl>
                <dt>Temps</dt>
                <dd>{{ weather['weather'][0]['description'] }} <img v-bind:src="getIcon()" /></dd>
            </dl>
            <dl>
                <dt>Température</dt>
                <dd>{{ weather['main']['temp'] }}°C</dd>
            </dl>
            <dl>
                <dt>Vitesse du vent</dt>
                <dd>{{ weather['wind']['speed'] }} km/h</dd>
            </dl>
        </div>
        
Et afin de gérer notre icone de temps, nous allons ajouter la méthode suivante :

        getIcon: function() {
            return 'http://openweathermap.org/img/w/'+this.weather['weather'][0]['icon']+'.png';
        }
        
## Obtenir de l'aide avec JavaScript :
- Mozilla MDN | site de référence pour les normes du web : https://developer.mozilla.org/fr-FR/docs/Web/JavaScript
- W3School | site de tutoriel pour apprendre à programmer : https://www.w3schools.com/jS/default.asp
- Vue.js | documentation du framework Vue.js : https://vuejs.org/v2/guide/
- W3C | Organisme de normalisation du web : https://www.w3.org/standards/webdesign/script

**[Partie suivante](../sauvegarder-mettre-en-ligne/README.md)**