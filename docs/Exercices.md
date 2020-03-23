Dans Sigil, « Ouvrir » ouvre des fichiers EPUB. Pour ajouter du contenu (fichier texte xhtml, feuille de style CSS, etc.) au contenu du fichier EPUB, utilisez « Ajouter fichiers existants ».

- **Exercice 1 :** mettre en page *Cyrano de Bergerac*. Utilisez le fichier `Cyrano.html` qui se trouve [dans le dépôt du TD](https://github.com/infologie/cours-epub). Ce texte est dans le domaine public.
- **Exercice 2 :** mettre en page *Qu'est-ce que la documentation ?*. Le texte est [en ligne](http://martinetl.free.fr/suzannebriet/questcequeladocumentation/). Une copie se trouve également dans le dépôt du TD. Il faut inclure les mentions légales : quelle est l'édition originale, qui a rédigé la préface et les notes de cette édition en ligne. Cela doit se faire à la fois au niveau des métadonnées et en début de texte (par un exemple sous forme d'un chapitre « Avant-propos »).

## Texte et couverture

Lorsque vous avez un fichier unique contenant l'intégralité du texte, il faut le découper en unités correspondant au chapitrage du fichier EPUB final : ceci crée le premier niveau de la table des matières. Chaque « chapitre » peut lui-même contenir des titres de différents niveaux qu'on peut décider de faire figurer dans la table des matières ou pas.

La fonction « Scinder au curseur » de Sigil sépare le fichier courant en deux fichiers distincts : le premier contient ce qui se trouve avant le curseur et le second ce qui se trouve après (pensez à une division cellulaire). Les deux fichiers ont exactement la même structure XHTML et notamment les modifications que vous avez faites dans le `head` et au niveau de la balise `body`. Une stratégie efficace consiste donc à faire ces modifications d'abord, puis scinder.

Créez une image de couverture avec les outils de votre choix et ajoutez-la à l'EPUB via Sigil. Regardez attentivement la façon dont elle est intégrée dans le modèle EPUB 3 du *framework* Blitz.

Exemples non contractuels et légèrement parodiques :

![](assets/images/coverCyrano.png)
![](assets/images/coverBriet.png)

## Espace insécables

Voici un bon exemple de modification qui va bien plus vite avec les bons outils.

Avec une expression régulière, remplacez tous les espaces avant des deux-points `:`, après un guillemet ouvrant `«` et avant un guillemet fermant `»`, par la chaîne de caractères `&#160;` (espace insécable).

**Solution :**

Rechercher : `(«) | ([»:])`  
Remplacer : `\1\&#160;\2`

Avec une expression régulière, remplacez tous les espaces avant des points-virgules `;`, des points d'interrogation `?` et des points d'exclamation `!` par la chaîne de caractères `&#8201;` (espace insécable fine).

**Solution :**

Rechercher : `\ ([;?!])` (attention à ne pas oublier l'espace au début)  
Remplacer : `\&#8201;\1`

## Mise en forme

Faites la liste de tous les éléments HTML utilisés dans le texte. Ils doivent tous faire l'objet d'une déclaration, ne serait-ce que pour maîtriser leur affichage par défaut. Blitz fait cela très bien via son *reset* initial.

**Petites majuscules** Dans *Cyrano*, chaque réplique est énoncée par un personnage dont le nom est déjà balisé par un span. Mettez ce nom en petites majuscules. Il faut trouver la propriété CSS en question (consultez le [MDN](https://developer.mozilla.org/fr/docs/Web/CSS/)) et utiliser une expression régulière pour l'appliquer partout.

Dans *Qu'est-ce que la documentation ?* les noms cités par Suzanne Briet étaient en petites majuscules dans le texte imprimé mais sont balisés en gras dans la version en ligne. Rétablissez les petites majuscules en remplaçant le gras par un *span* et une classe CSS, toujours en vous aidant d'expressions régulières.

**Polices de caractères** Appliquez au texte une pile de polices présentes dans différents systèmes de lecture *(system font stack)*. Choisissez parmi celles définies dans `blitz.css`. Faites de même pour les titres mais mettez en première position une police que vous inclurez manuellement dans l'EPUB.

## Assemblage

Faites en sorte que la **table des matières** permette d'accéder à tous les niveaux de titre du texte.

Renseignez les **métadonnées** dont vous disposez : titre et auteur. De plus, créditez-vous comme contributeur (`dc:contributor`). Vous pouvez préciser votre rôle (`opf:role`) via ce que Sigil appelle une propriété de métadonnée. Pour rappel liste des codes est ici : <https://www.loc.gov/marc/relators/relaterm.html>. Réfléchissez à ce dont vous êtes responsable dans ce fichier (balisage& ? design graphique& ?) et choisissez le code le plus approprié en conséquence.