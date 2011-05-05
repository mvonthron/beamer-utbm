UTBM : thème pour Beamer (LaTeX)
================================
Manuel Vonthron - <manuel DOT vonthron AT acadis DOT org>
Version 0.1 - 2010

Rémy HUBSCHER - <remy DOT hubscher AT ionyse DOT com>
Version 1.0 - 2011


INSTALLATION
------------
* Copier le dossier beamer-utbm dans le répertoire des thèmes Beamer
  (le dossier example/ peut être enlevé pour alléger)
    ex : /usr/share/texmf/tex/latex/beamer/themes/theme/
        (exécuter `locate Warsaw.sty` devrait indiquer le bon chemin)
* Mettre à jour l'index TeX (selon votre distribution LaTeX)
    ex : `texhash`
        (peut nécessiter les droits root)


UTILISATION
-----------
Appeler le thème "UTBM" après la déclaration de classe Beamer. Le cas
échéant, choisir la palette de couleurs à utiliser.

ex:
  \documentclass{beamer}
  \usetheme{UTBM}
  \usecolortheme{UTBMOfficial}


* Il est nécessaire de passer l'option 'plain' à l'environnement accueillant
  la page de titre afin de partir d'une "page blanche".
  ex:
    \begin{frame}[plain]
      \titlepage
    \end{frame}


* Le texte à afficher dans la ligne située en dessous du titre de la
  présentation est passé par la commande \subtitle{}

* Le cas échéant, le nom de l'entreprise est passé via la commande \institute{}.

* Si le titre est trop long pour pouvoir être affiché correctement dans
  la ligne de "footer", il est conseillé de placer un titre court de 
  substitution dans la commande \title{}
  ex : \title[Titre court]{Titre très très très très long}



PALETTES
--------
Quatre palettes sont livrées avec le thème UTBM :
  * UTBMOfficial 
      Palette de couleur "officielle" du modèle pour les présentations.
      Tons rouges, jaunes.
      http://download.trunat.fr/UTBM/MASQUE_UTBM.pptx
  * UTBMInternship 
      Palette de couleur "officielle" du modèle pour les soutenances de stage.
      Tons violets, jaunes.
      http://www.utbm.fr/upload/gestionFichiers/STAGES/PPT_UTBM_ST08.ppt
  * Terra
      Dérivé de la palette "Terra?", GlueStudio, 2008
      Tons bleus et marrons
      http://colourlovers.com/palette/292482/Terra
  * Curiosity
      Tons rouges, mauves, verts.
      Dérivé de la palette "Curiosity Killed", Miaka, 2008
      http://colourlovers.com/palette/444487/Curiosity_Killed

L'utilisation de l'un ou l'autre des thèmes de couleur se fait par la
commande : \usecolortheme{}.


OPTIONS
-------
  * shownavigation=false|true
      Affiche ou non (par défaut) les boutons de navigation sur chaque
      slide (malheureusement y compris sur la page de titre pour l'instant).
  * logo={images/logo.pdf}
      Chemin vers le logo à afficher en bas à droite de la page de titre.
      Sera redimensionné à 2em de hauteur.
  * titlepageimage={images/titleimage.pdf}
      Image à afficher en haut de la page de titre (actuellement obligatoire).
      Sera redimensionné à la largeur de la page.
  * header={fullnav|shortnav|utbm}
      Type de header pour les dispositives normales :
      fullnav : affichage des sections et sous-sections
      shortnav : affichage des sections horizontalement
      utbm : affichage d'un simple bandeau "UTBM"
  * suiveur={}
      Dans le cas d'une soutenance de stage : affiche le nom du suiveur 
      UTBM en dessous du nom de l'auteur.
  * tuteur={}
      Dans le cas d'une soutenance de stage : affiche le nom du tuteur 
      UTBM en dessous du nom de l'auteur.
  * dept={}
      Ajoute le département (et/ou la filière) à droite du nom de l'auteur
