L'EPUB est un dossier compressé avec quelques fichiers spéciaux qui lui permettent d'être opéré comme un ensemble cohérent. Ainsi, le fichier `content.opf` déclare l'ensemble des normes, métadonnées et contenus utilisés dans l'EPUB, ainsi que l'ordre de lecture des fichiers. Quant au fichier `toc.ncx`, il indique la table des matières au système de lecture.

Un logiciel comme Sigil permet d'automatiser tout l'assemblage de l'EPUB, notamment en fournissant des interfaces à ces fichiers (génération des métadonnées, de la table des matières). Ceci n'empêche pas de jeter périodiquement un coup d'œil directement dedans pour vérifier que tout se passe bien.

La **validation** permet ensuite de s'assurer que le fichier EPUB ne comporte pas d'erreur et sera affichage par un système de lecture. En revanche, la manière dont il sera affiché peut varier, bien plus que ne varie l'affichage de sites web& ; c'est tout le défi du design de livre numérique. Il faut donc tester le fichier sur les types de plateformes pertinentes pour le public auquel il est destiné.

Pour la gestion et la lecture, deux suggestions parmi bien d'autres : [Calibre](https://calibre-ebook.com/) et [Thorium](https://www.edrlab.org/software/thorium-reader/).

## Liens utiles

### Dans le manuel FLOSS

- [« Créer un EPUB 3 »](https://fr.flossmanuals.net/creer-un-epub/epub-3/), qui décrit précisément à quoi sert chaque partie de l'EPUB.
- [« Vérifier la validité du fichier »](https://fr.flossmanuals.net/creer-un-epub/verifier-la-validite-du-fichier/)
