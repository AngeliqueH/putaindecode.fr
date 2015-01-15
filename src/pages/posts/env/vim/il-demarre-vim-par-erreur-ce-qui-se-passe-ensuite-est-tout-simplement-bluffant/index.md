> À première vue, vous allez éprouver de la tristesse, mais ce qui se passe ensuite est tout simplement incroyable...

> Alors qu’il était en train d'effectuer une mise en production,
ce développeur s'est confronté a une situation qui aurait pu complètement déraper.
Au lieu de fuir, l’homme a décidé de rester sur place, immobile,
afin de s’assurer que le problème qu'il devait régler le soit pour de bon :
la base de données de production était apparement corrompu !

> A ce moment précis, il n'y avait qu'une issue possible.
Notre développeur devait arranger la base de données par lui même.
Une intervention directement sur un serveur en production était obligatoire afin d'éditer le fichier .txt d'une taille d'environ 600Mo.

> Après avoir passé plusieurs heures pour se connecter à distance via une connexion sécurisée,
Maxime est tombé nez à nez avec une console d'administration en ligne de commande !
Lui qui croyait se trouver sur une bonne vieille interface de serveur Windows 2000,
il était complètement désemparé par l'absence de fenêtre.

> Ce qui s’est passé ensuite est tout simplement incroyable:
fort de sa persévérance, Maxime décide tout de même de se rapprocher du clavier !

> Après une rapide recherche sur les Internets,
il tape la première commande qu'il trouve

> ```console
> $ vim
> ```

> Alors qu'on pourrait imaginer un drame, comme il arrive souvent quand [une personne tombe dans ce piège](https://duckduckgo.com/?q=JE+SUIS+COINC%C3%89+DANS+VIM),
Maxime ne s'est pas laissé abattre et a persisté dans sa démarche...

Bon assez plaisanté. Vous vous doutez bien que c'est pas ça du tout en vrai.

## Pourquoi j'essayerais Vim ?

J'étais sous SublimeText avant d'essayer Atom (car en gros Atom est quasiment la même chose, en technologie web, open source et fait par GitHub).
Mais j'ai toujours eu envie de me la péter devant 2 écrans tout noir,
en ligne de commandes, comme dans les super productions américaines.

Plus sérieusement, je passe de plus en plus de temps devant ma console...
Devant mon terminal, pardon.

J'ai toujours eu envie de comprendre pourquoi autant de gens (car mine de rien il y en a un paquet) utilisaient Vim,
et se moquaient un bon coup à chaque sortie d'un nouvelle éditeur.
Car bon faut avouer, se moquer c'est facile.
Du coup un jour, j'ai démarré Vim.

## Pourquoi j'ai rien compris quand je me suis retrouvé dans Vim

Le truc le plus déroutant dans Vim, c'est les modes.
Et quand on ouvre Vim, on ne se retrouve pas dans le mode le plus logique (à première vue).

En fait ce qu'on dit pas trop, c'est que Vim est toujours utilisé aujourd'hui (entre autres) car on peut l'utiliser uniquement au clavier.
Vous allez me répondre qu'on peut en faire de même avec tous les éditeurs de texte.

Mais **Vim a clairement été développé pour minimiser les déplacements des mains**.

C'est pour moi la chose la plus importante à retenir. Et la chose la plus attractive.
Les bon développeurs ont tous une bonne flemme au fond d'eux, c'est bien connu.

Pour un peu plus sur l'histoire de Vim, direction https://fr.wikipedia.org/wiki/Vim .

## Commencer avec Vim

Bon bon c'est pas tout, mais du coup quand je suis dans Vim, comment ça se passe ?

Je vais aller assez rapidement sur les différents points, vu que d'autres ressources,
dont notammement le livre [Vim pour les humains](https://vimebook.com/) font très bien en douceur.

C'est d'ailleur grâce à ce livre que je me suis lancé.
Je tiens donc à remercier Vincent Jousse pour avoir pris le temps d'écrire cette ouvrage.

Profitez de cette ouvrage, en plus [le prix est libre](http://ploum.net/le-prix-libre-une-impossible-utopie/).

Ce livre est fait pour n'importe qui, débutant ou pas.
Vraiment, mangez-en si vous souhaitez essayer Vim (oui je sais, manger un e-book comme ça, ça paraît pas évident).

J'ai essayé plusieurs fois sans trop savoir où commencer sans succès.
Ce livre m'a aidé et se torche en quelques dizaines de minutes (un couple d'heures), clavier sous les mains (bah oui rien de mieux pour se lancer).

J'ai essayé et me voilà conquis, une fois que j'ai compris sa valeur ajoutée.

Pour bien s'y prendre, forcez-vous avez Vim au moins une journée en suivant les conseils que vous trouverez dans cette ouvrage.
Cela a fonctionné pour moi: je gagne déjà du temps au bout de ma 2e semaine d'utilisation.

Pourquoi pas vous ?

La suite de cette article est un condensé pour ce qui veulent survoler ou se rémémorér rapidement quelques points et astuces.

**Note: lorsque vous voyez `:` en début d'une commande, c'est qu'il s'agit d'une commande Vim et non juste d'un simple raccourcis clavier.
Vous verrez donc le reste de votre commande en bas de Vim.**

## Les commandes de bases pour se déplacer

En gros, il faut clairement oublier les flêches du clavier, car elles sont loin.

`hjkl` seront solicités (gauche, bas, haut, droite) pour se déplacer.
On s'y fait rapidement (le mieux étant de faire comme le propose Vincent, en désactivant les flêches un moment).

Ensuite voici quelques astuces:

- `:0` ou `gg`: aller au début d'un fichier
- `G`: aller à la fin du fichier
- `:10`: aller ligne 10
- `ctrl+f`: page down
- `ctrl+b`: page up
- `0`: aller en début de ligne
- `^`: aller en début de ligne (premier caractère)
- `$`: aller en fin de ligne
- `e`: aller en fin d'un mot
- `b`: aller au début du mot
- `w`: aller au début du mot suivant

Notez bien que la plupart des commandes peuvent être préfixé par un nombre pour executer la commande plusieurs fois.
Vous le verrez assez souvant dans les exemples ci-après.

Plus sur les déplacements dans Vim http://vim.wikia.com/wiki/Moving_around

## Les modes

### Mode normal

Mode par défaut, on peut y utiliser les touches `hjkl` pour se déplacer et saisir les commandes.
C'est le mode qu'on utilisera en fait assez souvant, dès qu'on voudra manipuler du texte (couper, coller, déplacer etc).

Quand on est un peu perdu dans Vim, on va en mode normal via <kbd>Esc</kbd>.

Tant qu'on y est :

- `:w`: sauvegarder
- `:q`: quitter
- `:wq`: sauvegarder et quitter
- `:wa`: sauvegarder tous les fichiers ouverts (vous trouverez comment éditer plusieurs fichiers juste après).

Si vous voulez quitter sans sauvegarder, on force avec `!`: `:q!`.

### Mode insertion

Le mode insertion permet de saisir du texte. Vous verrez `-- INSERT --`. Dans la barre de commande de Vim.

Pour aller en mode insertion vous avez les touches suivantes disponibles (quand vous êtes en mode normal).

- `i`: insérer à la position du curseur
- `a`: insérer après la position du curseur
- `I`: insérer en début de ligne
- `A`: insérer en fin de ligne
- `o`: insérer dans une nouvelle ligne en dessous
- `O`: insérer dans une nouvelle ligne en dessus

### Mode visuel

Utiliser `v` pour passer en mode visuel (`-- VISUAL --`).
Il permet de sélectionner du texte.

Vous pouvez utiliser les raccourcis habituels pour vous déplacer, puis les raccourcis suivants pour agir sur la séléction.

## Quelques examples de commandes

### Copier du texte

- `yy`: copier la ligne en cours (`y` seul en mode visuel pour copier la sélection).
- `5yy`: copier les 5 lignes à partir de la ligne en cours
- `y$`: copier jusqu'à la fin de la ligne

### Coller du texte

- `p` avant le curseur
- `P` après le curseur

### Couper du texte

- `dd`: copier la ligne en cours

cf Copier pour les combos.

### Supprimer du texte

- `"_dd`: notez qu'il faut rajouter `"_` pour que le delete ne se place pas dans le presse-papier vim (`"_`: black hole).

## Copier du texte vers le presse-papier système

On va `yank` avec un prefix (`"+`) pour prévenir Vim. Exemple :

- `"+10yy` pour copier 10 lignes vers le presse-papier système.

Notez que remplacer + par * devrait fonctionner aussi bien.

Si vous avez des problèmes (exemple: avec OS X) vous pouvez utiliser ce bind :

```
" `ctrl+c/ctrl+v to share clipboard with OSX
vmap <C-c> y:call system("pbcopy", getreg("\""))<CR>
nmap <C-v> :call setreg("\"",system("pbpaste"))<CR>p
```

Source: http://vim.wikia.com/wiki/Accessing_the_system_clipboard 

## Coller du texte depuis le presse-papier système

Votre raccourci habituel de l'OS  va faire ce que vous voulez, sauf si vous avez l'option `autoindent`.
Dans ce cas, une petite commande pour dire à vim que vous allez coller du brute qu'il ne doit pas toucher :

`:set paste`

Une fois votre code collé :

`:set nopaste`

## Inverser 2 lignes

En utilisant tout ce qu'on a appris avant, on peut simplement faire:

- `ddp`: inverser la ligne courante avec celle du dessous
- `kddp`: inverser la ligne courante avec celle du dessus

## Déplacer un block de code

On peut certes faire la même chose dans les autres éditeurs, mais en couplant avec d'autres raccourcis/commandes,
on peut imaginer:

- `:10<enter>5dd:20<enter>p`: aller ligne 10, couper 5 lignes de code, puis les coller ligne 20.

## Interface utilisateur

Dans tout éditeur, on se doit d'avoir une UI pour se balader de fichier en fichier

### Avoir plusieurs fichiers

Tab ?
Pas vraiment mais équivalent avec les **Buffers**

`:set hidden`: avoir plusieurs buffers ouvert en même temps, ouvrir un buffer cache le précédent.
Vous devriez inclure cela dans votre .vimrc.

`:edit basededonnee.txt`: ouvrir un fichier dans un nouveau buffer.
Avec l'option précédente, on peut ouvrir plusieurs fichiers dans différents "tampons" mais n'en avoir qu'un devant soit.

`:bd`: supprimer le buffer en cours.

### Avoir plusieurs fenêtres

- `ctrl+w s`: couper à l'horizontal.
- `ctrl+w v`: couper à la vertical.

`:q` pour fermer une fenêtre. Ou quitter vim.

### Redimensionner des fenêtres

- `ctrl+w +`: augmenter la fenêtre d'une ligne
- `ctrl+w -`: diminuer la fenêtre d'une ligne
- `ctrl+w >`: augmenter la fenêtre d'une colonne
- `ctrl+w <`: diminuer la fenêtre d'une colonne

On peut bien sur combiner ca avec des multiplicateurs pour augmenter/diminuer des plusieurs lignes/colonnes

- `10 ctrl+w >`: augmenter de 10 colonnes
- `5 ctrl+w <`: diminuer de 5 lignes

#### Tout découper à part égale

Une fois qu'on a jouer avec la taille de fenêtre, on veut des fois juste avoir son écran coupé en 4/6/8 etc...
Rien de plus simple avec `=`.

`ctrl+w =`: découper tous les fenêtres aux mêmes dimensions.

Plus sur le découpage des fenêtres http://vim.wikia.com/wiki/Resize_splits_more_quickly


### Des tabs en plus de tout ça ?

Voilà de vrais tabs. En gros en plus des buffers et window,
vous pouvez avoir des tabs contenant des windows (qui eux contiennent des buffers).

Si si c'est simple.

- `:tabedit {file}`: éditer un fichier dans un nouvel onglet.
- `:tabfind {file}`: ouvrir un onglet correspondant au fichier.
- `:tabclose`: fermer l'onglet.
- `:tabclose {i}`: fermer l'onglet à la position donné.
- `:tabonly`: fermer tous les onglets sauf celui en cours.

Plus sur les onglets http://vim.wikia.com/wiki/Using_tab_pages

Note: personnellement je me satisfait des buffer/windows, et j'utilise les tabs de mon terminal.
En effet, je préfère avoir plusieurs sessions Vim (une session par projet, plus pratique pour les recherches par exemple).

### Rechercher dans un fichier

`/truc` pour chercher `truc` dans le fichier en cours

### Rechercher/remplacer dans le buffer en cours

- `s/truc/machin`: remplace le premier `truc` par `machin`.
- `s/truc/machin/g`: remplace `truc` par `machin` sur toute la ligne.
- `%s/truc/machin/g`: remplace `truc` par `machin` dans tout le fichier.

Pour faire les remplacements un par un vous pouvez ajouter le flag `c` (pour confirmation).

### Rechercher/remplacer  dans tous les fichiers

```
:arg *.md # selectionner les .md
:argadd *.txt # y ajouter les .txt
:arg  # vérifier la selection
:argdo %s/pattern/replace/ge | update # faire le remplacement
```

Plus sur le rechercher/remplacer  http://vim.wikia.com/wiki/Search_and_replace_in_multiple_buffers

### Rechercher dans le projet en cours (en restant dans Vim)

On peut utiliser `:grep` directement dans Vim, mais je n'ai pas trouvé l'interface très clair.
Voici donc comment j'ai fait autrement.

Cette manipulation d'[installer un plugin](#installer-un-plugin).

Pour Vim, le projet en cours c'est le dossier où nous avons ouvert le premier fichier (ou le dossier courant à défaut).
Pour voir le dossier en cours, il suffit de faire `:cwd`. On peut le changer avec la commande `cd` (eg: `:cd path/`).

Bon maintenant que vous savez où est le projet en cours, vous avez peut être envie de chercher dedans.
Pour ce faire on prend le plugin [ack](https://github.com/mileszs/ack.vim), puis on tente:

`:ack [options] {pattern} [{directories}]`

Vous noterez qu'on peut passer des options. Se référer à [la documentation Ack](http://beyondgrep.com/documentation/) pour en savoir plus.

Vous avez aussi remarqué que vous pouvez passer des dossiers en plus, pratique pour cibler une recherche dans une partie d'un projet.

## Gestion de fonctionnalités supplémentaires (plugins)

Que serait la plupart des éditeurs de texte sans leurs plugins ?

### Choisir un gestionnaire de plugin

Il existe plusieurs gestionnaires de plugins

- [Pathogen](https://github.com/tpope/vim-pathogen), le doyen des gestionnaires de plugins,
- [Vundle](https://github.com/gmarik/vundle), un autre, simple, un peu sur le bas côté à mes yeux,
- [NeoBundle](https://github.com/Shougo/neobundle.vim), basé sur Vundle, avec des améliorations
- [vim-addon-manager](https://github.com/MarcWeber/vim-addon-manager), qui a le mérite d'offrir l'autocomplétion pour les nom de plugins
- [oh-my-vim](https://github.com/gawel/oh-my-vim), encore un autre,
- [vim-plug](https://github.com/junegunn/vim-plug), un minimaliste, très simple à prendre en main.

Pour ma part j'ai choisi `vim-plug` car:

- il ne nécessite qu'une seul ligne dans le `.vimrc`,
- il est conscis et efficace,
- il serait le plus rapide à démarrer
- et permet mine de rien quelques trucs cool (lazyload, supporte les branches ou tag pour les plugins sur git

Si celui là vous dit, je vous renvoie [aux instructions](https://github.com/junegunn/vim-plug#usage) d'installation.

### Installer un plugin

Du coup quelque soit le manager que vous avez choisi,
on se contente en gros d'une ligne dans son `.vimrc`.

```vimrc
" use vim-plug to handle plugins
call plug#begin('~/.vim/plugged')

" generic config that everyone (should) use
Plug 'tpope/vim-sensible'
```

Ensuite il faut update la config de vim dans vim (en quittant ou en "sourçant" sa config) puis lancer l'installation

```vim
:source ~/.vimrc
:PlugInstall
```

Et paf

![vim-plug install](https://raw.githubusercontent.com/junegunn/i/master/vim-plug/installer.gif)

Une fois que c'est bon, on peut fermer la fenêtre en question (rappel: `:q`).

## Gestion de projets/session

Le plugin à avoir selon moi pour la gestion de projets c'est [vim-obsession](https://github.com/tpope/vim-obsession).
Une fois installé et activé sur un projet (`:Obsess`), il traquera votre session dans un fichier `Session.vim` afin que 
vous puissiez poursuivre votre session une fois Vim fermé et réouvert.

## Aller plus loin (recommandé)

Puis pour finir, voici un lien vers ma config vim versionné:

[MoOx/setup/dotfiles/vimrc](https://github.com/MoOx/setup/blob/master/dotfiles/vimrc)

Vous y trouverez des références vers d'autres configs intéressantes, ainsi que les plugins que j'utilise.
J'ai essayé d'y commenter comme il faut l'utilité des lignes un maximum. Si quelque chose n'est pas clair, n'hésitez pas à le signaler.

Pour apprendre Vim, vous pouvez aussi :

- jouer à [Vim adventure](http://vim-adventures.com/)
- lancer la commande `:vimtutor`
- lire l'ebook [Vim pour les humains](http://vimebook.com)

Prochaine étape: utiliser tmux en plus de Vim pour masteriser le terminal.
