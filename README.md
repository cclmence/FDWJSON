# FDWJSON
Repo pour PJ FDW

Vous devez réaliser un système permettant l’indexation et la recherche par le contenu de fichier SVG. Les fichiers SVG sont des fichiers XML contenant des informations sur les primitives graphiques qui composent une image vectorielle. Pour faire de telles images, vous pouvez notamment utiliser le logiciel libre Inkscape.

Votre système doit permettre de traiter les documents SVG pour les intégrer dans une base de données MongoDB. Vous devez proposer ensuite un système d’interrogation permettant de retrouver toutes les images possédant un rectangle ou une ellipse bleue par exemple, avec une interrogation Web. Le serveur web que vous devez utiliser est nodejs avec le plugin mongoose.
Ce travail se déroule en groupe de 3 personnes.

## Démarche  
Vous devrez dans un premier temps définir l’architecture de votre base de données JSON ainsi que le formalisme de représentation de ces images. Vous créerez ensuite un outil basé sur une feuille de style XSLT permettant d’extraire et représenter en JSON les formes formes de base d’une image SVG et de l’intégrer au sein de MongoDB. Enfin, vous devrez faire une interface d’interrogation Web simple permettant, au travers du serveur nodejs, de faire des recherches en fonction du contenu des images.
La représentation JSON de l’image SVG devra contenir la liste des formes de base et leurs caractéristique ainsi d’un lien vers / contenu du fichier SVG. 

Les formes de base de SVG sont :
- les rectangles
- les cercles
- les ellipses
- les lignes
- les lignes brisées («polylines»)
- les polygones

Toutes les informations nécessaire sur les formes de base SVG et les attributs sont disponibles sur :  
https://www.w3.org/TR/SVG/shapes.html

## Critères d’évaluation sur le logiciel  
- Design du modèle de données JSON (non redondance, choix des bonnes structures, etc).
- Qualité de la feuille de style XSLT : concision, robustesse, etc.
- Nombre et expressivité des requêtes ( au moins X requêtes, dont au moins une mixant la conjonction (ET) , disjonction(OU) et négation (NON)
- Commentaires sur le code et documentation sur déploiement du logiciel.

Les plus : 
Proposer des requêtes pour rechercher les documents contenant des formes imbriquées (un cercle contenu dans un rectangle, etc.)