La mise en forme comprend un travail de design graphique mais pas seulement. Il s'agit d'anticiper l'expérience de lecture en négociant les intentions de conception du designer et du système de lecture, ainsi que les intentions du lecteur.

> Design is not just what it looks like and feels like, design is how it works. Ebook Designers must take many hardware and software constraints into account, it’s not just about CSS. Jiminy Panoz, *[The ebook Design Checklist](https://friendsofepub.github.io/eBookDesignChecklist/)*

Un exemple : la CSS du *framework* [Blitz](https://friendsofepub.github.io/Blitz/). Stratégie utilisée : remplacer les paramètres par défaut par des bases saines respectant la spécification EPUB 3, puis construire le design en suivant le principe d'[amélioration progressive](https://fr.wikipedia.org/wiki/Am%C3%A9lioration_progressive).

Examinons ce que cible cette CSS très complète (les mots anglais en italique correspondent au sectionnement du fichier `blitz.css`) :

- l'**organisation de la pseudo-page** *(Page layout)*, notamment où interviennent les sauts de page *(Page breaks)* et les ruptures thématiques *(Horizontal rules — context breaks)* ;
- la **typographie** *(Typography)* et ses détails *(Micro typography)* ;
- les autres contenus textuels, qui ont une disposition spécifique, comme les listes *(Lists)*, listes de définitions *(Definition lists)*, tableaux *(Tables)* et fragments de code *(Code)* ;
- les **médias** en général *(Medias)*, les figures et images en particulier *(Figures + images)*.

Comme tout bon *framework*, cette CSS inclut des classes prédéfinies. Ce sont des utilitaires *(Utilities)* en général et des conteneurs *(Containers — wrappers)* en particulier. Elles permettent de régler localement différentes choses :

- la typographie, dont les familles de polices *(Font-stacks)*, alignement *(Text align)*, indentation *(Indents)*, tailles *(Font sizes)* et styles *(Font styles)*.
- les hauteurs *(Widths)* et largeurs *(Heights)* ;
- le type d'affichage *(Display)*, notamment celui des éléments flottants *(Floats)* et leur position *(Clearings)*,
- les bordures *(Bordered content)* et marges *(Margins)*.

## Liens utiles

### Dans le manuel FLOSS

- [« Typographie et mise en page »](https://fr.flossmanuals.net/creer-un-epub/ajouter-des-fontes/)

### Ailleurs

- [Documentation de Blitz CSS](https://friendsofepub.github.io/Blitz/documentation/docs.html#css-doc) (en anglais)
- [Référence CSS de Mozilla Developer Network](https://developer.mozilla.org/fr/docs/Web/CSS) (une grande partie traduite en français)
- [Référence CSS de W3Schools](https://www.w3schools.com/cssref/) (en anglais)