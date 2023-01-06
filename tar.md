<!-- metastart
Auteur  == loxcy
Version == 0.1
Date    == 2023/01/01 
endmeta -->
Tar
===
La commande tar est un outil puissant qui permet de créer, d'extraire et de manipuler des archives en Linux et Unix. Elle est souvent utilisée pour compresser et décompresser des fichiers, mais elle peut également être utilisée pour fusionner plusieurs fichiers en un seul, pour créer des copies de sauvegarde de fichiers ou pour transférer des fichiers d'un ordinateur à un autre.

## Utilisation de la commande tar:

```sh
## Compression d'un dossier en utilisant plusieurs threads:
tar -cjf archive.tar.bz2 -I pbzip2 folder/

## Extraction d'une archive en utilisant plusieurs threads:
tar -xjf archive.tar.bz2 -I pbzip2

   -c : permet de créer une nouvelle archive
   -x : permet d'extraire les fichiers d'une archive
   -f : permet de spécifier le nom du fichier d'archive
   -v : permet d'afficher la liste des fichiers inclus dans l'archive
   -z : permet de compresser l'archive en utilisant gzip
   -j : permet de compresser l'archive en utilisant bzip2
   -p : permet de copier les droits d'accès des fichiers dans l'archive
   -P : permet de créer l'archive en incluant le chemin complet des fichiers
--exclude: permet d'exclure certains fichiers ou dossiers de l'archive
--verify: permet de vérifier l'intégrité des fichiers inclus dans l'archive
```
*Il existe de nombreuses autres options disponibles pour la commande tar, qui vous permettent de personnaliser encore davantage son utilisation. Pour en savoir plus sur ces options, vous pouvez consulter la documentation de tar ou utiliser la commande tar --help pour afficher la liste complète des options disponibles.*

## Compression 

pigz, lbzip2 et pbzip2 sont tous des outils de compression et de décompression parallèles qui permettent d'utiliser plusieurs threads pour accélérer le processus de compression et de décompression de fichiers. Voici quelques différences clés entre ces outils:

    - pigz est une implémentation parallèle de l'outil de compression gzip. Il utilise la bibliothèque de compression ZLIB pour compresser et décompresser des fichiers. pigz est compatible avec l'option -z de la commande tar et peut être utilisé pour compresser et décompresser des fichiers au format .gz.  

    - lbzip2 est une implémentation parallèle de l'outil de compression bzip2. Il utilise l'algorithme de compression Burrows-Wheeler pour compresser et décompresser des fichiers. lbzip2 est compatible avec l'option -j de la commande tar et peut être utilisé pour compresser et décompresser des fichiers au format .bz2.

    - pbzip2 est également une implémentation parallèle de l'outil de compression bzip2. Tout comme lbzip2, il utilise l'algorithme de compression Burrows-Wheeler pour compresser et décompresser des fichiers. pbzip2 est compatible avec l'option -j de la commande tar et peut être utilisé pour compresser et décompresser des fichiers au format .bz2.

gzip et bzip2 sont tous deux des outils de compression de fichiers qui permettent de réduire la taille des fichiers en utilisant des algorithmes de compression. Voici quelques différences clés entre ces deux outils:

Algorithme de compression: gzip utilise l'algorithme de compression DEFLATE pour compresser et décompresser des fichiers, tandis que bzip2 utilise l'algorithme de compression Burrows-Wheeler.

Taux de compression: bzip2 offre généralement un taux de compression plus élevé que gzip, ce qui signifie que les fichiers compressés avec bzip2 ont généralement une taille plus petite que ceux compressés avec gzip. Cependant, bzip2 est également plus lent que gzip en raison de l'algorithme de compression plus complexe qu'il utilise.

En général, gzip est un outil de compression rapide et efficace qui convient bien aux fichiers de petite à moyenne taille. bzip2, quant à lui, est un outil de compression plus lent, mais offre un taux de compression plus élevé et convient donc mieux aux fichiers de grande taille. Vous pouvez choisir l'outil qui convient le mieux à vos besoins en fonction de la taille et du type de fichiers que vous souhaitez compresser.
