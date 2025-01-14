---
title: "Accueil"
---

# Création d'un portfolio simple en prenant avantage de la JamStack.


Avant de rentrer dans le vif du sujet, on présente rapidement le principe, les outils et la méthodologie. 


On parle de JamStack pour décrire un site créer en prenant avantage de plusieurs outils mis à disposition (gratuitement, en libre de droit, payant, avec abonnement, etc..) et en les assemblant afin de bénéficier de leurs avantages (et ne pas réinventer la roue à chaque contrainte). Par exemple, plutôt que de gérer manuellement l'hébergement de notre site, on utilise un outil comme Netlify qui le fait pour nous. L'idée, c'est de ne pas perdre de temps sur des fonctionnalités déjà existantes, et de se concentrer sur le design et le contenu de notre site.


Dans ce tutoriel, on va créer un site en utilisant les outils suivants : 


* [Github Desktop](https://desktop.github.com/download/) nous permet de gérer facilement notre projet, de créer des sauvegardes et différentes versions de travailles, ainsi que de stocker notre projet en ligne. On utilise la version desktop pour nous simplifier le travail, et ne pas avoir à apprendre les commandes Gits. 
* [Visual Studio Code](https://code.visualstudio.com/) pour notre éditeur de code. il nous permet de facilement faire le lien avec Github et Hugo. Il est tout à fait possible d'en utiliser un autre, mais c'est de loin de plus pratique.
* [Hugo](https://gohugo.io/), un framework ultra rapide et open source, qui nous permet de simplifier la construction d'un site web optimisé, avec des options de templating nous permettant de facilité la maintenabilité et les modifications du site.
* [Sveltia](https://github.com/sveltia/sveltia-cms/?tab=readme-ov-file#getting-started), c'est un projet se basant sur DecapCMS (anciennement [NetlifyCMS](https://www.netlify.com/blog/netlify-cms-to-become-decap-cms/)) et l'améliorant, notamment avec l'ajout d'un interface beaucoup plus poussé et de fonctionnalité de traitement d'images plus avancé. C'est grâce à Sveltia que l'on va pouvoir mettre à jour et ajouter du contenu sur notre site sans passer par un éditeur de code.
* [Netlify](https://www.netlify.com/), qui fait le lien avec notre répertoire Github où est stocké notre projet, pour le transformer en site internet disponible en ligne. 

## Mettre en place le projet


Une fois Github Desktop et Visual Studio Code installé, on va pouvoir mettre en place le projet. On se rend dans notre [espace personnel sur GitHub](https://github.com/) et on créer un nouveau répertoire en cliquant sur le bouton `New` en haut à gauche.


![Interface du dashboard Github](/dashboard-github.png "Interface du dashboard Github")


 Donner un nom à votre répertoire, dans notre exemple ce sera "*tutoriel_portfolio*", et validez en cliquant sur `Create repository` en bas à droite. (les autres options peuvent être laissés par défaut). 


![Création d'un répertoire dans l'interface github](/dashboard-github-etape-2.png "Création d'un répertoire dans l'interface github")


Si on retourne dans notre dashboard, on voit que notre nouveau répertoire est bien créé. 


![Dashboard de github avec le nouveau répertoire présent](/dashboard-github-etape-3.png "Dashboard de github avec le nouveau répertoire présent")


Maintenant, rendons nous dans Github Desktop. Si ce n'est pas déjà fait, connecter l'application à votre compte Github. Ensuite, on peut cloner notre répertoire afin de pouvoir travailler localement sur notre machine. \
En haut à gauche, on clique sur `File > Clone repository`.


![Interface de github desktop, clonage d'un répertoire ](/github-desktop-etape-1.png "Interface de github desktop, clonage d'un répertoire")


On choisit le répertoire que l'on a créé plus tôt et on clique sur `Clone` en bas de la fenêtre. 


![Choix d'un répertoire dans github desktop ](/github-desktop-etape-2.png "Choix d'un répertoire dans github desktop")


Une fois le répertoire cloné, on peut constater que l'on se trouve bien dans le bon espace de travail en haut à gauche (et passer d'un projet à un autre si besoin). On peut maintenant ouvrir notre projet dans VScode en cliquant dans le bouton `Open in Visual Studio Code` au centre de l'écran.


![Interface de github desktop une fois un répertoire cloné](/github-desktop-etape-3.png "Interface de github desktop une fois le répertoire cloné")


Et voilà, on est prêt à travailler ! On pourrait s'arrêter là et faire un site internet statique en créant des pages en HTML, en les personnalisant avec des feuilles de styles CSS et en ajoutant de l'interaction en Javascript. Mais avant de faire ça, on va installer Hugo afin de nous faciliter la vie. 


***Avant de continuer, fermez GitHub Desktop et Visual Studio Code.***