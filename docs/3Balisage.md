Cette étape correspond aussi à la modification du texte pour respecter des conventions mais d'un langage informatique cette fois-ci (le XHTML). Cela repose sur une bonne connaissance des [éléments HTML 5](https://developer.mozilla.org/fr/docs/Web/Guide/HTML/HTML5/Liste_des_%C3%A9l%C3%A9ments_HTML5).

Les éléments dont le nom décrit quelque chose qui existe indépendamment de HTML (titres, paragraphes, listes, emphase…) correspondent à du balisage sémantique. Ils représentent la majorité des éléments HTML. On peut y ajouter des attributs comme `epub:type` et `role`, qui permettent de préciser encore la sémantique et d'améliorer l'accessibilité.

Exemple : `<section epub:type="chapter" role="doc-chapter">`

L'**accessibilité** n'est pas un détail. Vous pouvez explorer ce sujet en cherchant le mot-clé « a11y » (pour *accessibility*) un peu partout sur le web. Le format EPUB peut intégrer des enrichissements sémantiques respectant la spécification [ARIA](https://fr.wikipedia.org/wiki/Accessible_Rich_Internet_Applications), ce qui facilite son utilisation au sein d'interfaces spécifiques (synthèse vocale, navigation).

Les éléments qui n'ont pas vraiment de signification propre (*divs* et *spans*) servent à appliquer des classes et identifiants : c'est le balisage destiné à la mise en forme. Il va de pair avec la rédaction des feuilles de style CSS (voir étape suivante).

Exemple : `<span class="small-caps">`

## Liens utiles

### Dans le manuel FLOSS

- [« Les bases du HTML et du CSS pour l'EPUB »](https://fr.flossmanuals.net/creer-un-epub/specificites-du-css-pour-lepub/)

### Ailleurs

- [Référence HTML de Mozilla Developer Network](https://developer.mozilla.org/fr/docs/Web/HTML) (une grande partie traduite en français)
- [Référence HTML de W3Schools](https://www.w3schools.com/tags/default.asp) (en anglais)

Sur l'accessibilité :

- IDPF (2017) [Techniques d’Accessibilité EPUB 1.0](http://www.edrlab.org/public/sne/TAE_HTML_V3/Techniques_d_Accessibilite_EPUB%201.0.htm) (en anglais). Très complet. Renvoie vers toutes les autres publications IDPF et W3C traitant d'accessibilité. Explique toutes les techniques possibles et recommandées. La longueur de la page peut faire peur mais c'est un avantage : tout est au même endroit, donc les informations cherchées se retrouvent rapidement via <kbd>Ctrl</kbd> + <kbd>F</kbd>.
- Le travail de [Luc Maumet](http://maumet.fr/), notamment en matière de veille.