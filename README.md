# Découpe CNC


## Étapes_pour_la_découpe_CNC

1- Modélisation par exemple avec Sketchup ou un autre permettant une exportation en format STL.

2- Avec Sketchup il faut télécharger le plugin SketchUcam du site http://www.phlatforum.com/viewtopic.php?f=98&t=2. Il est nécessaire de se créer un profil sur leur site pour télécharger.

3- Produire dans sketchup un développement du modèle à découper de manière à ce que chaque pièce soit développée à plat.

4- Réglez les paramètres du plugin SketchUcam , en particulier le diamètre de l'outil qui est en général de 0,1250 Po, 1/8 Po. et la vitesse et le percage à 2-12 Po/min, et l'épaisseur du matériel à la dimension de votre panneau en général 1/4 Po 0,25.

5- Effectuer un tracé Intérieur ou Extérieur pour l'outil suivant les besoins avec SketchUcam

6- Avec SketchUcam et son outil GCode produire un fichier .CNC comprenant les GCodes.

7- Téléchargez l'outil CncUsb du site http://www.planet-cnc.com/index.php?page=download de manière a simuler la coupe, Ouvrez votre fichier .cnc et faire view > simulate Réglez au besoin la vitesse avec view > simulate > increase/decrease speed.

8- Au lab téléchargez votre fichier .cnc sur le PC du Phlatprinter et ouvrez le avec CncUsb 

9- Positionnez votre panneau sous les rouleaux de la Phlatprinter au centre de la machine et serrez les guides sans exces.Fixez solidement le couteau au mandarin de la toupie. Mettez des lunettes et protecteurs auditifs. En utilisant le JOG et après vous etre assuré du réglage de la vitesse de déplacement positionnez la pointe du couteau pour effleurer la surface du matériau. Toujours en utilisant le JOG déplacez la position X et Y de manière à positionnez la pointe du couteau l'extérieur de votre panneau dans le coin bas droit à environ 2 Po  en X et Y. 

10- Dans CncUsb ouvrir File>Setting>General et réglez Po ou mm suivant le besoin. Faites le Zéro du logiciel CncUsb, vérifiez et réglez si nécessaire la vitesse d'avance en cochant Override et démarrez la marche de  CncUsb. Votre coupe s'effectue, assurez vous de dépoussiérer avin d'éviter l'introduction de tas de débris sous les rouleaux ce qui favorise le glissement.


## Couches logicielles pour la découpe CNC

ÉchoFab dispose d'une découpeuse automatique  Phlatprinter capable de découper à plat des matériaux tel le Mdf ou l'acrylique à une épaisseur d'environ 1/4 de Po X 36 Po X 36 Po. De façon universelle, un fichier au format CNC doit être produit afin de diriger le processus de traitement.

Idéalement, le fichier Sketchup doit montrer les pièces développées à plat.

SketchUcam un plugin Sketchup va permettre de placer des marges autour des pièces d'y introduire des ponts de support et de produire le code Cnc qui sera ensuite transféré sur le Pc de contrôle du de la Phlatprinter équipé du logiciel CncUsb auquel le fichier .cnc sera soumis et permettra de contröler la coupeuse.


Étapes: Design --> Développement --> Ajout des marges, Tab --> Création du G-Code --> Découpe

## Notes pour la CNC

  * Si on souhaite une découpe précise, 1/8" ou mieux, il est important d'utiliser un couteau dont les arêtes sont en bon état. Si les arêtes sont émoussées le couteau aura tendance à forcer le coupe biaisant dans le sens de la rotation à cause de la trop forte friction.
  * De même pour une coupe précise il est important d'utiliser une vitesse d'avance du couteau adaptée au matériau et à la précision désirée. Dans du MDF 1/4" pour une coupe précise, une avance de 6"/min est adéquate.

## Liste de vérification


**Liste de vérification Phlatprinter**

  - Fermer le porte du local pour limiter le bruit
  - Avertir les occupants de porter des protecteurs audifs
  - Démarrer le PC de la CNC, charger CNC-USB et ouvrir votre fichier .cnc
  - Désalimenter l'électronique et la toupie.
  - Installer et aligner le matériau à couper sur le lit de la Phlat.
  - Ajuster les guides latéraux.
  - Remonter manuellement la toupie et installer le couteau.
  - Placer manuellement la pointe du couteau au zéro X/Y/Z
  - Alimenter l'électronique de la Phlat.
  - S'assurer de la communication PC-CNC dans le programme CNC-USB
  - Vérifier et ajuster si nécessaire la vitesse d'avance de l'outil dans CNC-USB et faire Override


S'il est souhaité de faire un dry-run jogger relever l'axe dez Z+


Sinon

  - Faire le zéro dans dans la colonne d'outils de CNC-USB.
  - Porter des protecteurs auditifs
  - Porter des lunettes de protection
  - Porter un masque respiratoire.
  - Démarrer l'aspirateur et positionner le boyau.
  - Alimenter la toupie de la Phlat.
  - Faire Start dans la ligne de menu de CNC-USB.
  - Surveiller le tracé en dépoussiérant.

A la fin du tracé stopper la toupie et l'électronique de la Phlat.

## Log_CNC

#### Utilisations
  * Découpe de matériaux (Foam) maximum 1/2".
  * Découpe de matériaux mous (Crèpe / Mousse)
  * Dessin avec pointe de feutre

#### Objectifs
  * Pointe pour métal 
  * Pointe pour lame d'exacto
  * Pointe pour crayon peinture (graffiti)

#### Idées
  * Utiliser des crayons pour dessiner (Plans / Pochoir / Stencil)
  * Utiliser un pointe pour perforer des stencil et créer des 

#### Problèmes
  * Problème de mèche lors de découpe de bois de plus d'1/4"

  * InkScape converti mal les fichier Jpeg en Vectoriel
On doit nettoyer avec Illustrator les multiples lignes créer par la conversion.

## Cnc et Acrylique 

Quelques infos en vrac, surtout pour m'en souvenir:

[[http://www.frezycnc.eu/micro-end-mills-applications/signmakers-end-mills-set/cutters-for-plexiglass-all-thermoplastics/|Méches]]


[[http://www.cnczone.com/forums/glass_plastic_stone/46102-need_advice_routing_plexiglass.html|Source]]

9500 RPM
Feedrate: 8 mm/s (19 IPM)
Depth of cut: 2mm (5/64")

For a 1/8" 2 flute router
9500 RPM
Feedrate: 20 mm/s (47 IPM)
Depth of cut: 1.5mm (around 1/16")

Outil qui permet de trouver la bite appropriée
http://www.plasticrouting.com/BitSearch.asp?Page=Brand

The main factors in preventing acrylic from melting while machining, from my experience, are:

  * As high a feed rate as possible [[200-300|ipm]]
  * Low spindle speed [[2000-3500|rpm]]


Et finalement un petit pdf léger en lecture de chevet
http://www.engraverssolutions.com/PDFs/tips&tricks-routing_acrylic.pdf
