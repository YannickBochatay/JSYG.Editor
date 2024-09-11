# JSYG.Editor

Editor of svg shapes with [JSYG framework](https://github.com/YannickBochatay/JSYG)

If you look for a complete SVG editor with very simple API, try [JSYG.FullEditor](https://github.com/YannickBochatay/JSYG.FullEditor).
This one is just a brick.

### Demo

<http://yannickbochatay.github.io/JSYG.Editor/>

### Installation

```shell
npm install jsyg-editor
```

### Usage

##### with module bundler

```javascript
import Editor from "jsyg-editor"

let editor = new Editor("#mySVGContainer");
editor.enable({
  list:"#mySVGContainer > [data-editable]"
  ctrls:"all"
});
```

### API

<!-- Generated by documentation.js. Update this documentation by updating the source code. -->

##### Table of Contents

*   [Editor](#editor)
    *   [Parameters](#parameters)
    *   [onchangetarget](#onchangetarget)
    *   [onbeforeshow](#onbeforeshow)
    *   [onshow](#onshow)
    *   [onbeforehide](#onbeforehide)
    *   [onhide](#onhide)
    *   [onupdate](#onupdate)
    *   [onstart](#onstart)
    *   [ondragstart](#ondragstart)
    *   [ondrag](#ondrag)
    *   [ondragend](#ondragend)
    *   [onend](#onend)
    *   [onchange](#onchange)
    *   [setNode](#setnode)
        *   [Parameters](#parameters-1)
    *   [target](#target)
        *   [Parameters](#parameters-2)
    *   [targetRemove](#targetremove)
        *   [Parameters](#parameters-3)
    *   [isMultiSelection](#ismultiselection)
    *   [list](#list)
    *   [hide](#hide)
        *   [Parameters](#parameters-4)
    *   [show](#show)
        *   [Parameters](#parameters-5)
    *   [update](#update)
        *   [Parameters](#parameters-6)
    *   [enableCtrls](#enablectrls)
    *   [disableCtrls](#disablectrls)
    *   [align](#align)
        *   [Parameters](#parameters-7)
*   [editor](#editor-1)
*   [CtrlPoints](#ctrlpoints)
    *   [Parameters](#parameters-8)
    *   [editor](#editor-2)
    *   [list](#list-1)
    *   [container](#container)
    *   [className](#classname)
    *   [shape](#shape)
    *   [xlink](#xlink)
    *   [width](#width)
    *   [height](#height)
    *   [linked](#linked)
    *   [draggableOptions](#draggableoptions)
    *   [onshow](#onshow-1)
    *   [onhide](#onhide-1)
    *   [onstart](#onstart-1)
    *   [ondragstart](#ondragstart-1)
    *   [ondrag](#ondrag-1)
    *   [ondragend](#ondragend-1)
    *   [onend](#onend-1)
    *   [enabled](#enabled)
    *   [display](#display)
    *   [on](#on)
    *   [off](#off)
    *   [trigger](#trigger)
    *   [enable](#enable)
        *   [Parameters](#parameters-9)
    *   [disable](#disable)
    *   [show](#show-1)
        *   [Parameters](#parameters-10)
    *   [hide](#hide-1)
        *   [Parameters](#parameters-11)
    *   [update](#update-1)
*   [MainPoints](#mainpoints)
    *   [Parameters](#parameters-12)
    *   [editor](#editor-3)
    *   [list](#list-2)
    *   [container](#container-1)
    *   [className](#classname-1)
    *   [shape](#shape-1)
    *   [width](#width-1)
    *   [height](#height-1)
    *   [classNameClosing](#classnameclosing)
    *   [strengthClosingMagnet](#strengthclosingmagnet)
    *   [autoSmooth](#autosmooth)
    *   [onshow](#onshow-2)
    *   [onhide](#onhide-2)
    *   [onstart](#onstart-2)
    *   [ondragstart](#ondragstart-2)
    *   [ondrag](#ondrag-2)
    *   [ondragend](#ondragend-2)
    *   [onend](#onend-2)
    *   [draggableOptions](#draggableoptions-1)
    *   [on](#on-1)
    *   [off](#off-1)
    *   [trigger](#trigger-1)
    *   [enabled](#enabled-1)
    *   [display](#display-1)
    *   [enable](#enable-1)
        *   [Parameters](#parameters-13)
    *   [disable](#disable-1)
    *   [show](#show-2)
        *   [Parameters](#parameters-14)
    *   [hide](#hide-2)
        *   [Parameters](#parameters-15)
    *   [update](#update-2)
*   [Drag](#drag)
    *   [Parameters](#parameters-16)
    *   [editor](#editor-4)
    *   [type](#type)
    *   [bounds](#bounds)
    *   [options](#options)
    *   [multiple](#multiple)
    *   [onstart](#onstart-3)
    *   [ondragstart](#ondragstart-3)
    *   [ondrag](#ondrag-3)
    *   [ondragend](#ondragend-3)
    *   [onend](#onend-3)
    *   [on](#on-2)
    *   [off](#off-2)
    *   [trigger](#trigger-2)
    *   [enabled](#enabled-2)
    *   [display](#display-2)
    *   [enable](#enable-2)
        *   [Parameters](#parameters-17)
    *   [disable](#disable-2)
    *   [start](#start)
        *   [Parameters](#parameters-18)
    *   [show](#show-3)
        *   [Parameters](#parameters-19)
    *   [hide](#hide-3)
    *   [update](#update-3)
*   [Resize](#resize)
    *   [Parameters](#parameters-20)
    *   [editor](#editor-5)
    *   [list](#list-3)
    *   [stepsX](#stepsx)
    *   [stepsY](#stepsy)
    *   [container](#container-2)
    *   [className](#classname-2)
    *   [shape](#shape-2)
    *   [xlink](#xlink-1)
    *   [width](#width-2)
    *   [height](#height-2)
    *   [type](#type-1)
    *   [multiple](#multiple-1)
    *   [onshow](#onshow-3)
    *   [onhide](#onhide-3)
    *   [onstart](#onstart-4)
    *   [ondragstart](#ondragstart-4)
    *   [ondrag](#ondrag-4)
    *   [ondragend](#ondragend-4)
    *   [onend](#onend-4)
    *   [horizontal](#horizontal)
    *   [vertical](#vertical)
    *   [keepRatio](#keepratio)
    *   [bounds](#bounds-1)
    *   [options](#options-1)
    *   [on](#on-3)
    *   [off](#off-3)
    *   [trigger](#trigger-3)
    *   [enabled](#enabled-3)
    *   [display](#display-3)
    *   [enable](#enable-3)
        *   [Parameters](#parameters-21)
    *   [disable](#disable-3)
    *   [show](#show-4)
        *   [Parameters](#parameters-22)
    *   [hide](#hide-4)
        *   [Parameters](#parameters-23)
    *   [update](#update-4)
*   [canHideMainPoints](#canhidemainpoints)
    *   [Parameters](#parameters-24)
*   [Rotate](#rotate)
    *   [Parameters](#parameters-25)
    *   [editor](#editor-6)
    *   [list](#list-4)
    *   [steps](#steps)
    *   [container](#container-3)
    *   [className](#classname-3)
    *   [shape](#shape-3)
    *   [xlink](#xlink-2)
    *   [width](#width-3)
    *   [height](#height-3)
    *   [multiple](#multiple-2)
    *   [cursor](#cursor)
    *   [onshow](#onshow-4)
    *   [onhide](#onhide-4)
    *   [onstart](#onstart-5)
    *   [ondragstart](#ondragstart-5)
    *   [ondrag](#ondrag-5)
    *   [ondragend](#ondragend-5)
    *   [onend](#onend-5)
    *   [options](#options-2)
    *   [on](#on-4)
    *   [off](#off-4)
    *   [trigger](#trigger-4)
    *   [enabled](#enabled-4)
    *   [display](#display-4)
    *   [enable](#enable-4)
        *   [Parameters](#parameters-26)
    *   [disable](#disable-4)
    *   [show](#show-5)
        *   [Parameters](#parameters-27)
    *   [hide](#hide-5)
        *   [Parameters](#parameters-28)
    *   [update](#update-5)

#### Editor

<strong>nécessite le module Editor</strong>
Edition d'éléments (positionnement, dimensions, rotation, et édition des formes pour les éléments SVG).

##### Parameters

*   `arg`  argument JSYG canvas des éléments à éditer
*   `opt`  optionnel, objet définissant les options.

Returns **[Editor](#editor)**&#x20;

##### onchangetarget

Fonctions à exécuter quand on définit une autre cible

##### onbeforeshow

Fonctions à exécuter avant l'affichage de la boite d'édition (renvoyer false pour empecher l'événement)

##### onshow

Fonctions à exécuter à l'affichage de la boite d'édition

##### onbeforehide

Fonctions à exécuter avant la suppression de la boite d'édition (renvoyer false pour empecher l'événement)

##### onhide

Fonctions à exécuter à la suppression de la boite d'édition

##### onupdate

Fonctions à exécuter à la mise à jour de la boite d'édition

##### onstart

Fonctions à exécuter à chaque fois qu'une action d'édition se prépare, qu'elle est lieu ou non (mousedown sur un contrôle)

##### ondragstart

Fonctions à exécuter à chaque fois qu'une action d'édition débute

##### ondrag

Fonctions à exécuter pendant une action d'édition

##### ondragend

Fonctions à exécuter à la fin d'une action d'édition

##### onend

Fonctions à exécuter au relachement du bouton de souris, qu'il y ait eu modification ou non

##### onchange

Fonctions à exécuter à tout changement

##### setNode

définit le canvas d'édition

###### Parameters

*   `arg`  argument JSYG

Returns **[Editor](#editor)**&#x20;

##### target

définit ou renvoie l'élément à éditer

###### Parameters

*   `arg`  argument JSYG optionnel, si renseigné définit la cible à éditer
*   `_preventEvent` &#x20;

##### targetRemove

Réinitialise la cible

###### Parameters

*   `_preventEvent` &#x20;

##### isMultiSelection

Indique si plusieurs éléments sont édités à la fois

Returns **[Boolean](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Boolean)**&#x20;

##### list

définit ou renvoie la liste des éléments éditables dans le canvas.

##### hide

Masque le conteneur d'édition

###### Parameters

*   `e` &#x20;
*   `_preventEvent` &#x20;

##### show

Affiche le conteneur d'édition

###### Parameters

*   `e`  optionnel, objet Event afin de commencer tout de suite le déplacement de l'élément
    (ainsi sur un meme événement mousedown on peut afficher le conteneur et commencer le déplacement)
*   `_preventEvent` &#x20;

Returns **[Editor](#editor)**&#x20;

##### update

Mise à jour du conteneur d'édition. (Si l'élément est modifié par un autre moyen que les contrôles du conteneur,
il peut s'avérer utile de mettre à jour le conteneur)

###### Parameters

*   `e` &#x20;
*   `_preventEvent` &#x20;

Returns **[Editor](#editor)**&#x20;

##### enableCtrls

Activation des contrôles.<br/>
appelée sans argument, tous les contrôles sont activés. Sinon, en arguments (nombre variable) les noms des contrôles à activer
('drag','resize','rotate','ctrlPoints','mainPoints').

##### disableCtrls

Désactivation des contrôles.<br/>
appelée sans argument, tous les contrôles sont desactivés. Sinon, en arguments (nombre variable) les noms des contrôles à desactiver
('Drag','Resize','Rotate','CtrlPoints','MainPoints').

##### align

Aligne les éléments sélectionnés

###### Parameters

*   `type` **[String](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/String)** (top,middle,bottom,left,center,right)

Returns **[Editor](#editor)**&#x20;

#### editor

référence vers l'objet Editor parent

#### CtrlPoints

Edition des points de contrôle des chemins SVG

##### Parameters

*   `editorObject` &#x20;

##### editor

référence vers l'objet Editor parent

##### list

liste des contrôles

##### container

Conteneur des contrôles

##### className

Classe appliquée au conteneur des contrôles

##### shape

Forme utilisée pour les contrôles

##### xlink

lien utilisé si shape est défini à "use"

##### width

largeur du contrôle

##### height

hauteur du contrôle

##### linked

Points de contrôle liés ou non (si on en déplace un, l'autre se déplace en miroir)

##### draggableOptions

*   **See**: {Draggable}

Options supplémentaires pour le drag\&drop

##### onshow

Fonction(s) à exécuter à l'affichage des contrôles

##### onhide

Fonction(s) à exécuter à la suppression des contrôles

##### onstart

Fonction(s) à exécuter quand on prépare un déplacement (mousedown sur le contrôle)

##### ondragstart

Fonction(s) à exécuter quand on commence un déplacement

##### ondrag

Fonction(s) à exécuter pendant le déplacement

##### ondragend

Fonction(s) à exécuter en fin de déplacement

##### onend

Fonction(s) à exécuter au relâchement de la souris, qu'il y ait eu modification ou non

##### enabled

Indique si les contrôles sont activés ou non

##### display

Indique si les contrôles sont affichés ou non

##### on

*   **See**: JSYG.StdConstruct.prototype.on

Ajout d'écouteurs d'événements customisés

Returns **[CtrlPoints](#ctrlpoints)**&#x20;

##### off

*   **See**: JSYG.StdConstruct.prototype.on

Retrait d'écouteurs d'événements customisés

Returns **[CtrlPoints](#ctrlpoints)**&#x20;

##### trigger

*   **See**: JSYG.StdConstruct.prototype.trigger

Déclenche un événement customisé

##### enable

Activation des contrôles

###### Parameters

*   `opt`  optionnel, objet définissant les options

Returns **[CtrlPoints](#ctrlpoints)**&#x20;

##### disable

Désactivation des contrôles

Returns **[CtrlPoints](#ctrlpoints)**&#x20;

##### show

Affichage des contrôles

###### Parameters

*   `opt`  optionnel, objet définissant les options
*   `_preventEvent` &#x20;

Returns **[CtrlPoints](#ctrlpoints)**&#x20;

##### hide

Masque les contrôles

###### Parameters

*   `_preventEvent` &#x20;

Returns **[CtrlPoints](#ctrlpoints)**&#x20;

##### update

Met à jour les contrôles

Returns **[CtrlPoints](#ctrlpoints)**&#x20;

#### MainPoints

Edition des points principaux des chemins SVG

##### Parameters

*   `editorObject` &#x20;

##### editor

référence vers l'objet Editor parent

##### list

liste des contrôles

##### container

Conteneur des contrôles

##### className

Classe appliquée au conteneur des contrôles

##### shape

Forme utilisée pour les contrôles

##### width

largeur des contrôles

##### height

hauteur des contrôles

##### classNameClosing

classe appliquée au dernier point d'un chemin si le chemin est fermé

##### strengthClosingMagnet

Force de la magnétisation entre les points extremes pour fermer le chemin

##### autoSmooth

Lisse automatiquement les chemins

##### onshow

Fonction(s) à exécuter à l'affichage des contrôles

##### onhide

Fonction(s) à exécuter à la suppression des contrôles

##### onstart

Fonction(s) à exécuter quand on prepare un déplacement (mousedown sur le contrôle)

##### ondragstart

Fonction(s) à exécuter quand on commence un déplacement

##### ondrag

Fonction(s) à exécuter pendant le déplacement

##### ondragend

Fonction(s) à exécuter en fin de déplacement

##### onend

Fonction(s) à exécuter au relachement de la souris, qu'il y ait eu modification ou non

##### draggableOptions

*   **See**: {Draggable}

Options supplémentaires pour le drag\&drop

##### on

*   **See**: JSYG.StdConstruct.prototype.on

Ajout d'écouteurs d'événements customisés

Returns **[MainPoints](#mainpoints)**&#x20;

##### off

*   **See**: JSYG.StdConstruct.prototype.on

Retrait d'écouteurs d'événements customisés

Returns **[MainPoints](#mainpoints)**&#x20;

##### trigger

*   **See**: JSYG.StdConstruct.prototype.trigger

Déclenche un événement customisé

##### enabled

Indique si les contrôles sont activés ou non

##### display

Indique si les contrôles sont affichés ou non

##### enable

Activation des contrôles

###### Parameters

*   `opt`  optionnel, objet définissant les options

Returns **[MainPoints](#mainpoints)**&#x20;

##### disable

Désactivation des contrôles

Returns **[MainPoints](#mainpoints)**&#x20;

##### show

Affichage des contrôles

###### Parameters

*   `opt`  optionnel, objet définissant les options
*   `_preventEvent` &#x20;

Returns **[MainPoints](#mainpoints)**&#x20;

##### hide

Masque les contrôles

###### Parameters

*   `_preventEvent` &#x20;

Returns **[MainPoints](#mainpoints)**&#x20;

##### update

Met à jour les contrôles

Returns **[MainPoints](#mainpoints)**&#x20;

#### Drag

déplacement de l'élément

##### Parameters

*   `editorObject` &#x20;

##### editor

référence vers l'objet Editor parent

##### type

Type de déplacement ("attributes" ou "transform" pour agir sur les attributs de mise en page ou sur la matrice de transformation)

##### bounds

Permet de limiter le déplacement à l'intérieur de l'offsetParent (null pour annuler, valeur numérique négative pour aller au delà de l'offsetParent)

##### options

*   **See**: {Draggable}

Options supplémentaires pour le drag\&drop

##### multiple

Indique si ce contrôle est actif dans le cas d'une sélection multiple

##### onstart

Fonction(s) à exécuter quand on prépare un déplacement (mousedown sur le contrôle)

##### ondragstart

Fonction(s) à exécuter quand on commence un déplacement

##### ondrag

Fonction(s) à exécuter pendant le déplacement

##### ondragend

Fonction(s) à exécuter en fin de déplacement

##### onend

Fonction(s) à exécuter au relachement de la souris, qu'il y ait eu déplacement ou non

##### on

*   **See**: JSYG.StdConstruct.prototype.on

Ajout d'écouteurs d'événements customisés

Returns **[Drag](#drag)**&#x20;

##### off

*   **See**: JSYG.StdConstruct.prototype.on

Retrait d'écouteurs d'événements customisés

Returns **[Drag](#drag)**&#x20;

##### trigger

*   **See**: JSYG.StdConstruct.prototype.trigger

Déclenche un événement customisé

##### enabled

Indique si le controle est activé ou non

##### display

Indique si le contrôle est affiché ou non

##### enable

Activation du contrôle

###### Parameters

*   `opt`  optionnel, objet définissant les options

##### disable

Désactivation du contrôle

Returns **[Drag](#drag)**&#x20;

##### start

commence le drag\&drop

###### Parameters

*   `e`  objet Event

Returns **[Drag](#drag)**&#x20;

##### show

Affiche le contrôle

###### Parameters

*   `opt`  optionnel, objet définissant les options

##### hide

Masque le contrôle

Returns **[Drag](#drag)**&#x20;

##### update

Met à jour le contrôle

Returns **[Drag](#drag)**&#x20;

#### Resize

Edition des dimensions

##### Parameters

*   `editorObject` &#x20;

##### editor

référence vers l'objet Editor parent

##### list

liste des contrôles

##### stepsX

liste des paliers horizontaux (largeurs en px)

##### stepsY

liste des paliers verticaux (hauteurs en px)

##### container

Conteneur des contrôles

##### className

Classe appliquée au conteneur des contrôles

##### shape

Forme utilisée pour les contrôles

##### xlink

lien utilisé si shape est défini à "use"

##### width

largeur des contrôles

##### height

hauteur des contrôles

##### type

Type de déplacement ("attributes" ou "transform" pour agir sur les attributs de mise en page ou sur la matrice de transformation)

##### multiple

Indique si ce contrôle est actif dans le cas d'une sélection multiple

##### onshow

Fonction(s) à exécuter à l'affichage des contrôles

##### onhide

Fonction(s) à exécuter à la suppression des contrôles

##### onstart

Fonction(s) à exécuter quand on prépare un déplacement (mousedown sur le contrôle)

##### ondragstart

Fonction(s) à exécuter quand on commence un déplacement

##### ondrag

Fonction(s) à exécuter pendant le déplacement

##### ondragend

Fonction(s) à exécuter en fin de déplacement

##### onend

Fonction(s) à exécuter au relaéchement de la souris, qu'il y ait eu modification ou non

##### horizontal

définit si l'élément est redimensionnable horizontalement

##### vertical

définit si l'élément est redimensionnable verticalement

##### keepRatio

définit si le ratio doit etre conservé

##### bounds

Permet de limiter le redimensionnement à l'intérieur de l'offsetParent (null pour annuler, valeur numérique négative pour aller au delà de l'offsetParent)

##### options

*   **See**: {Resizable}

Options supplémentaires pour le redimensionnement

##### on

*   **See**: JSYG.StdConstruct.prototype.on

Ajout d'écouteurs d'événements customisés

Returns **[Resize](#resize)**&#x20;

##### off

*   **See**: JSYG.StdConstruct.prototype.on

Retrait d'écouteurs d'événements customisés

Returns **[Resize](#resize)**&#x20;

##### trigger

*   **See**: JSYG.StdConstruct.prototype.trigger

Déclenche un événement customisé

##### enabled

Indique si les contrôles sont activés ou non

##### display

Indique si les contrôles sont affichés ou non

##### enable

Activation des contrôles

###### Parameters

*   `opt`  optionnel, objet définissant les options

Returns **[Resize](#resize)**&#x20;

##### disable

Désactivation des contrôles

Returns **[Resize](#resize)**&#x20;

##### show

Affichage des contrôles

###### Parameters

*   `opt`  optionnel, objet définissant les options
*   `_preventEvent` &#x20;

Returns **[Resize](#resize)**&#x20;

##### hide

Masque les contrôles

###### Parameters

*   `_preventEvent` &#x20;

Returns **[Resize](#resize)**&#x20;

##### update

Met à jour les contrôles

Returns **[Resize](#resize)**&#x20;

#### canHideMainPoints

Pour les lignes simples, les poignées de controle masquent les extrémités à déplacer

##### Parameters

*   `node` **type**&#x20;

Returns **[Boolean](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Boolean)**&#x20;

#### Rotate

Edition de la rotation

##### Parameters

*   `editorObject` &#x20;

##### editor

référence vers l'objet Editor parent

##### list

liste des contrôles

##### steps

liste des paliers

##### container

Conteneur des contrôles

##### className

Classe appliquée au conteneur des contrôles

##### shape

Forme utilisée pour les contrôles

##### xlink

lien utilisé si shape est défini à "use"

##### width

largeur des contrôles

##### height

hauteur des contrôles

##### multiple

Indique si ce contrôle est actif dans le cas d'une sélection multiple

##### cursor

Curseur à appliquer à l'élément de contrôle

##### onshow

Fonction(s) à exécuter à l'affichage des contrôles

##### onhide

Fonction(s) à exécuter à la suppression des contrôles

##### onstart

Fonction(s) à exécuter quand on prépare un déplacement (mousedown sur le contrôle)

##### ondragstart

Fonction(s) à exécuter quand on commence un déplacement

##### ondrag

Fonction(s) à exécuter pendant le déplacement

##### ondragend

Fonction(s) à exécuter en fin de déplacement

##### onend

Fonction(s) à exécuter au relachement de la souris, qu'il y ait eu modification ou non

##### options

*   **See**: {Rotatable}

Options supplémentaires pour la rotation

##### on

*   **See**: JSYG.StdConstruct.prototype.on

Ajout d'écouteurs d'événements customisés

Returns **[Rotate](#rotate)**&#x20;

##### off

*   **See**: JSYG.StdConstruct.prototype.on

Retrait d'écouteurs d'événements customisés

Returns **[Rotate](#rotate)**&#x20;

##### trigger

*   **See**: JSYG.StdConstruct.prototype.trigger

Déclenche un événement customisé

##### enabled

Indique si les contrôles sont activés ou non

##### display

Indique si les contrôles sont affichés ou non

##### enable

Activation des contrôles

###### Parameters

*   `opt`  optionnel, objet définissant les options

Returns **[Rotate](#rotate)**&#x20;

##### disable

Désactivation des contrôles

Returns **[Rotate](#rotate)**&#x20;

##### show

Affichage des contrôles

###### Parameters

*   `opt`  optionnel, objet définissant les options
*   `_preventEvent` &#x20;

Returns **[Rotate](#rotate)**&#x20;

##### hide

Masque les contrôles

###### Parameters

*   `_preventEvent` &#x20;

Returns **[Rotate](#rotate)**&#x20;

##### update

Met à jour les contrôles

Returns **[Rotate](#rotate)**&#x20;
