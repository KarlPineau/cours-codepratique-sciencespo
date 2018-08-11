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

## Structuration du body :
- Les principales balises de structure :
  - header : https://developer.mozilla.org/fr/docs/Web/HTML/Element/header
  - main : https://developer.mozilla.org/fr/docs/Web/HTML/Element/main
  - footer : https://developer.mozilla.org/fr/docs/Web/HTML/Element/footer
  - section : https://developer.mozilla.org/fr/docs/Web/HTML/Element/section
  - article : https://developer.mozilla.org/fr/docs/Web/HTML/Element/article
  - aside : https://developer.mozilla.org/fr/docs/Web/HTML/Element/aside
  - nav : https://developer.mozilla.org/fr/docs/Web/HTML/Element/nav

- Notre structuration :

      <body>
          <header>
              <h1 title="Ce texte s'affiche au survol">Découvrez la mission Dakar-Djibouti</h1>
          </header>
          <main>
              <section>

              </section>
              <section>

              </section>
          </main>
          <footer>

          </footer>
      </body>

## Nos premières sections :
### Section 1 : présentation de la mission Dakar-Djibouti :
- Texte repris de Wikipédia pour la [description de la mission](https://fr.wikipedia.org/wiki/Mission_Dakar-Djibouti) :
> Une loi du 31 mars 1931 crée une Mission ethnographique et linguistique Dakar-Djibouti ; son objet officiel est de compléter les collections du musée d'ethnographie du Trocadéro afin de créer une vitrine savante de la colonisation.
> Parmi les membres de l'équipe de départ, deux participent de façon éphémère. Jean Moufle démissionne le 29 octobre 1931 et le prince Oukhtomsky tombe malade et est évacué le 11 juillet 1931. Outre Marcel Griaule, les membres permanents de la mission sont Michel Leiris, André Schaeffner, Deborah Lifchitz, Éric Lutten, Jean Mouchet et Gaston-Louis Roux. Abel Faivre rejoint l'équipe au Soudan anglo-égyptien le 16 mai 1932.
> Il s'agit pour une équipe composée de linguistes, d'ethnographes, d'un musicologue, d'un peintre, d'un naturaliste et d'un responsable des prises de vue cinématographiques, de traverser le continent d'ouest en est, du Sénégal à l'Éthiopie, afin de collecter un maximum de données ethnographiques. On compte ainsi plus de 3 000 objets rapportés et déposés au musée d'ethnographie du Trocadéro, ainsi que 6 000 photographies, 1 600 mètres de films et 1 500 fiches manuscrites.
> Ce projet scientifique commandé par l'État français (loi du 31 mars 1931) avait également des visées politiques et économiques : asseoir la position française en Afrique, notamment en Afrique de l'Est, et s'opposer de cette façon à l'influence grandissante de la couronne britannique sur ce continent.
> Plusieurs expéditions de Griaule ont ensuite suivi celle-ci : la Mission Sahara-Soudan (1935), puis la Mission Sahara-Cameroun (1936-1937) et enfin la Mission Niger-Lac Iro (1938-1939).
- Les balises que nous allons utiliser :
  - `<h2>` : [Titre de second niveau](https://developer.mozilla.org/fr/docs/Web/HTML/Element/h2), nous y plaçons notre intitulé de section : `<h2>Contexte de l'expédition</h2>` ;
  - `p` : [Paragraphe](https://developer.mozilla.org/fr/docs/Web/HTML/Element/p), nous y plaçons nos blocs de texte de description ainsi que notre source : `<p>Source : Wikipédia, consulté le 21 juillet 2018</p>` ;
  - `em` : [Emphase](https://developer.mozilla.org/fr/docs/Web/HTML/Element/em), le texte précisant notre source n'est pas n'importe quel texte, nous allons insister dessus : `<p><em>Source : Wikipédia, consulté le 21 juillet 2018</em></p>` ;
  - `a` : [Lien hypertexte](https://developer.mozilla.org/fr/docs/Web/HTML/Element/a), puisque notre source est en ligne, autant en donner directement le lien : `<p><em>Source : <a href="https://fr.wikipedia.org/wiki/Mission_Dakar-Djibouti">Wikipédia, consulté le 21 juillet 2018</a></em></p>`. Vous constatez qu'on utilise l'attribut `href` pour indiquer l'URL de notre lien ;
  - `blockquote` : [Block de citation](https://developer.mozilla.org/fr/docs/Web/HTML/Element/blockquote), dans lequel nous allons placer les paragraphes de notre texte de présentation.

**Ce qui nous donne au final :**

    <section>
        <h2>Contexte de l'expédition</h2>
        <article>
            <p><em>Source : <a href="https://fr.wikipedia.org/wiki/Mission_Dakar-Djibouti">Wikipédia, consulté le 21 juillet 2018</a></em></p>
            <blockquote cite="https://fr.wikipedia.org/wiki/Mission_Dakar-Djibouti">
                <p>Une loi du 31 mars 1931 crée une Mission ethnographique et linguistique Dakar-Djibouti ; son objet officiel est de compléter les collections du musée d'ethnographie du Trocadéro afin de créer une vitrine savante de la colonisation.</p>
                <p>Parmi les membres de l'équipe de départ, deux participent de façon éphémère. Jean Moufle démissionne le 29 octobre 1931 et le prince Oukhtomsky tombe malade et est évacué le 11 juillet 1931. Outre Marcel Griaule, les membres permanents de la mission sont Michel Leiris, André Schaeffner, Deborah Lifchitz, Éric Lutten, Jean Mouchet et Gaston-Louis Roux. Abel Faivre rejoint l'équipe au Soudan anglo-égyptien le 16 mai 1932.</p>
                <p>Il s'agit pour une équipe composée de linguistes, d'ethnographes, d'un musicologue, d'un peintre, d'un naturaliste et d'un responsable des prises de vue cinématographiques, de traverser le continent d'ouest en est, du Sénégal à l'Éthiopie, afin de collecter un maximum de données ethnographiques. On compte ainsi plus de 3 000 objets rapportés et déposés au musée d'ethnographie du Trocadéro, ainsi que 6 000 photographies, 1 600 mètres de films et 1 500 fiches manuscrites.</p>
                <p>Ce projet scientifique commandé par l'État français (loi du 31 mars 1931) avait également des visées politiques et économiques : asseoir la position française en Afrique, notamment en Afrique de l'Est, et s'opposer de cette façon à l'influence grandissante de la couronne britannique sur ce continent.</p>
                <p>Plusieurs expéditions de Griaule ont ensuite suivi celle-ci : la Mission Sahara-Soudan (1935), puis la Mission Sahara-Cameroun (1936-1937) et enfin la Mission Niger-Lac Iro (1938-1939). </p>
            </blockquote>
        </article>
    </section>

### Section 2 : la liste des membres de l'expédition :
- La liste des membres, leur rôle, et leur page Wikipédia pour ceux qui en ont une :
  - **André Schaeffner**, anthropologue, ethnomusicologue, https://fr.wikipedia.org/wiki/Andr%C3%A9_Schaeffner
  - **Deborah Lifchitz**, linguiste, https://en.wikipedia.org/wiki/Deborah_Lifchitz
  - **Michel Leiris**, écrivain, ethnologue, https://fr.wikipedia.org/wiki/Michel_Leiris
  - **Marcel Griaule**, ethnologue, https://fr.wikipedia.org/wiki/Marcel_Griaule
  - **Éric Lutten**, ethnologue, https://fr.wikipedia.org/wiki/%C3%89ric_Lutten
  - **Jean Mouchet**, linguiste, ethnologue, https://fr.wikipedia.org/wiki/Jean_Mouchet
  - **Gaston-Louis Roux**, dessinateur & peintre, https://fr.wikipedia.org/wiki/Gaston-Louis_Roux
  - **Abba Jérôme Gabra Mussié**, lettré éthiopien, interprête
  - **Marcel Larget**, naturaliste
  - **Abel Faivre**, géographe et naturaliste
- Les balises que nous allons utiliser :
  - `<h2>` : [Titre de second niveau](https://developer.mozilla.org/fr/docs/Web/HTML/Element/h2), nous y plaçons notre intitulé de section : `<h2>Les membres de l'expédition</h2>` ;
  - `<ul>` : [Liste à puces](https://developer.mozilla.org/fr/docs/Web/HTML/Element/h2), dans laquelle nous plaçons les membres. Si nous avions voulu une liste ordonnée, nous aurions utilisé `<ol>` ;
  - `<li>` : [Elément de liste](https://developer.mozilla.org/fr/docs/Web/HTML/Element/li), il y a donc une balise `<li>` par membre : `<li>Abel Faivre, géographe et naturaliste</li>` ;
  - `<a>` : [Lien hypertexte](https://developer.mozilla.org/fr/docs/Web/HTML/Element/a), lorsque nous possédons un lien vers une page Wikipédia : `<li><a href="https://fr.wikipedia.org/wiki/Andr%C3%A9_Schaeffner">André Schaeffner</a>, anthropologue, ethnomusicologue</li>` ;
  - `<img/>` : [Image](https://developer.mozilla.org/fr/docs/Web/HTML/Element/img), pour afficher la photographie de l'équipe, qui se trouve dans notre dossier `media` : `<img src="media/membres.jpg" alt="Les membres de l'expédition Dakar-Djibouti avant le départ" />`. Vous constatez que nous utilisons ici deux attributs :
    - `src`: Il s'agit de la source de notre image, autrement dit son URL. Comme l'image est sur notre ordinateur, nous donnons son chemin ;
    - `alt`: Le texte alternatif de l'image, à afficher lorsque l'image ne peut pas l'être. Par exemple pour les personnes non voyantes. Ce sont les deux attributs obligatoires pour une image.
  
**Ce qui nous donne au final :**

    <section>
          <h2>Les membres de l'expédition</h2>

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

          <img src="media/membres.jpg" alt="Les membres de l'expédition Dakar-Djibouti avant le départ" />
      </section>

### Mettons un peu de contenu dans notre footer :
- Notre texte : `Mini-site réalisé dans la joie et l'allégresse par les étudiants de Sciences Po'.`
- Notre balise : `<p>`, [Paragraphe](https://developer.mozilla.org/fr/docs/Web/HTML/Element/p) dont vous constatez que la balise sert à présenter n'importe quel bloc de texte.

**Ce qui nous donne au final :**

    <footer>
        <p>Mini-site réalisé dans la joie et l'allégresse par les étudiants de Sciences Po'.</p>
    </footer>
    
## Complétons le contenu de notre présentation :
### Le parcours de l'expédition :
- Le contenu de notre tableau est divisé en 4 colonnes : la date, la ville, le pays, le nombre collecté à ce point. Ce qui nous donne : 
Date |Ville |Pays |Objets collectés
-----|------|-----|-----------------
19 mai 1931 | Bordeaux | France | -
31 mai | Dakar | Sénégal | 41
14 juin | Tambacounda | - | 181
28 juin | Kayes | Mali | 242
17 juillet | Kita | - |414
- Nous allons utiliser les balises suivantes :
  - À vous de mettre en place les balises pour :
    - le titre de la section
    - la source : Jean Jamin, Le cercueil de Queequeg, Mission Dakar-Djibouti, mai 1931-février 1933, Les Carnets de Bérose, 2014, http://www.berose.fr/IMG/pdf/jj_6-09web.pdf
  - `<table>`, [Tableau](https://developer.mozilla.org/fr/docs/Web/HTML/Element/table) : il s'agit de la balise indiquant que l'on construit un tableau
  - `<thead>`, [En-tête](https://developer.mozilla.org/fr/docs/Web/HTML/Element/thead) de notre tableau. Il contient des lignes `<tr>`.
  - `<tbody>`, [Corps](https://developer.mozilla.org/fr/docs/Web/HTML/Element/tbody) de notre tableau. Il contient des lignes `<tr>`.
  - `<caption>`, [Légend](https://developer.mozilla.org/fr/docs/Web/HTML/Element/caption) de notre tableau.
  - `<tr>`, [Ligne](https://developer.mozilla.org/fr/docs/Web/HTML/Element/tr) de notre tableau.
  - `<td>`, [Cellule classique](https://developer.mozilla.org/fr/docs/Web/HTML/Element/td) de notre tableau. Se trouve dans une ligne `<tr>`.
  - `<th>`, [En-tête](https://developer.mozilla.org/fr/docs/Web/HTML/Element/th) de notre tableau. Se trouve dans une ligne `<tr>`.
- À savoir sur les tableaux :
  - On marque les cellules vides (c'est-à-dire qu'on écrit `<td></td>`) ;
  - On peut fusionner des cellules en utilisant les attributs `rowspan` (fusionner des cellules horizontalement) et `colspan` (fusionner des cellules verticalement), et l'on indique comme valeur de l'attribut le nombre de cellules à fusionner. La règle ci-dessus ne s'applique plus, si on fusionne 3 cellules, on n'écrit qu'un seul `<td rowspan=3></td>`.
- Exemple de code simple :

      <table>
          <caption>Parcours de l'expédition Dakar-Djibouti</caption>
          <thead>
          <tr>
              <th>Date</th>
              <th>Ville</th>
              <th>Pays</th>
              <th>Objets collectés</th>
          </tr>
          </thead>
          <tbody>
          <tr>
              <td>19 mai 1931</td>
              <td>Bordeaux</td>
              <td>France</td>
              <td></td>
          </tr>
          </tbody>
      </table>
 
 **Nous obtenons au final**
 
    <section>
        <h2>Le parcours de l'expédition</h2>

        <table>
            <caption>Parcours de l'expédition Dakar-Djibouti</caption>
            <thead>
            <tr>
                <th>Date</th>
                <th>Ville</th>
                <th>Pays</th>
                <th>Objets collectés</th>
            </tr>
            </thead>
            <tbody>
            <tr>
                <td>19 mai 1931</td>
                <td>Bordeaux</td>
                <td>France</td>
                <td></td>
            </tr>
            <tr>
                <td>31 mai</td>
                <td>Dakar</td>
                <td>Sénégal</td>
                <td>41</td>
            </tr>
            <tr>
                <td>14 juin</td>
                <td>Tambacounda</td>
                <td>-</td>
                <td>181</td>
            </tr>
            <tr>
                <td>28 juin</td>
                <td>Kayes</td>
                <td>Mali</td>
                <td>242</td>
            </tr>
            <tr>
                <td>17 juillet</td>
                <td>Kita</td>
                <td>-</td>
                <td>414</td>
            </tr>
            <tr>
                <td>4 août</td>
                <td>Bamako</td>
                <td>-</td>
                <td>1040</td>
            </tr>
            <tr>
                <td>31 août</td>
                <td>Sikasso</td>
                <td>-</td>
                <td>1258</td>
            </tr>
            <tr>
                <td>3 septembre</td>
                <td>Koutiala</td>
                <td>-</td>
                <td>1342</td>
            </tr>
            <tr>
                <td>4 septembre</td>
                <td>Ségou</td>
                <td>-</td>
                <td>1400</td>
            </tr>
            <tr>
                <td>10 septembre</td>
                <td>Mopti</td>
                <td>-</td>
                <td>1686</td>
            </tr>
            <tr>
                <td>21 septembre</td>
                <td>Djenné</td>
                <td>-</td>
                <td>1784</td>
            </tr>
            <tr>
                <td>28 septembre</td>
                <td>Sanga</td>
                <td>-</td>
                <td>2104</td>
            </tr>
            <tr>
                <td>28 novembre</td>
                <td>-</td>
                <td>-</td>
                <td></td>
            </tr>
            <tr>
                <td>30 novembre</td>
                <td>Ouagadouhou</td>
                <td>Haute-Volta</td>
                <td></td>
            </tr>
            <tr>
                <td>4 décembre</td>
                <td>Natitingou</td>
                <td>Dahomey</td>
                <td>2149</td>
            </tr>
            <tr>
                <td>6 décembre</td>
                <td>Djougou</td>
                <td>-</td>
                <td>2184</td>
            </tr>
            <tr>
                <td>11 décembre</td>
                <td>Cotonou</td>
                <td>-</td>
                <td>2411</td>
            </tr>
            <tr>
                <td>21 décembre</td>
                <td>Niamey</td>
                <td>Niger</td>
                <td>2492</td>
            </tr>
            <tr>
                <td>27 décembre</td>
                <td>Birni Nkoni</td>
                <td>-</td>
                <td>2513</td>
            </tr>
            <tr>
                <td>1er janvier 1932</td>
                <td>Mora</td>
                <td>Cameroun</td>
                <td>2575</td>
            </tr>
            <tr>
                <td>12 janvier</td>
                <td>Garoua</td>
                <td>-</td>
                <td>2787</td>
            </tr>
            <tr>
                <td>21 février</td>
                <td>Ebolowa</td>
                <td>-</td>
                <td>2792</td>
            </tr>
            <tr>
                <td>1er mars</td>
                <td>Bertoua</td>
                <td>-</td>
                <td>2813</td>
            </tr>
            <tr>
                <td>9 mars</td>
                <td>Bangui</td>
                <td>Oubangui-Chari</td>
                <td>2819</td>
            </tr>
            <tr>
                <td>14 mars</td>
                <td>Bambari</td>
                <td>-</td>
                <td>2830</td>
            </tr>
            <tr>
                <td>15 mars</td>
                <td>Bangassou</td>
                <td>-</td>
                <td>2867</td>
            </tr>
            <tr>
                <td>24 mars</td>
                <td>Bondo</td>
                <td>Congo belge</td>
                <td>2883</td>
            </tr>
            <tr>
                <td>28 mars</td>
                <td>Juba</td>
                <td>Soudan Anglo-Egyptien</td>
                <td>3034</td>
            </tr>
            <tr>
                <td>20 avril</td>
                <td>Gallabat</td>
                <td>-</td>
                <td>3049</td>
            </tr>
            <tr>
                <td>1er juillet</td>
                <td>Gondar</td>
                <td>Ethiopie</td>
                <td>3218</td>
            </tr>
            <tr>
                <td>19 décembre</td>
                <td>-</td>
                <td>-</td>
                <td></td>
            </tr>
            <tr>
                <td>22 décembre</td>
                <td>Agordat</td>
                <td>Erythrée</td>
                <td></td>
            </tr>
            <tr>
                <td>10 janvier 1933</td>
                <td>Djibouti</td>
                <td></td>
                <td></td>
            </tr>
            <tr>
                <td>17 février 1933</td>
                <td>Djibouti</td>
                <td>France</td>
                <td>3600</td>
            </tr>
            </tbody>
        </table>
        <p><em>Source : <a href="http://www.berose.fr/IMG/pdf/jj_6-09web.pdf">Jean Jamin, Le cercueil de Queequeg, Mission Dakar-Djibouti, mai 1931-février 1933, Les Carnets de Bérose, 2014</a></em></p>
    </section>

## Présentation du résultat final

## Allons-y
