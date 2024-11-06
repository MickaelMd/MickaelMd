## Liste des événements JavaScript courants avec addEventListener

### Événements liés à la souris

**click :** Se déclenche lorsqu'un élément est cliqué.

```js

document.getElementById('element').addEventListener('click', function() {
  console.log('Élément cliqué');
});
  
```

**dblclick :** Se déclenche lorsqu'un élément est double-cliqué.

```js

document.getElementById('element').addEventListener('dblclick', function() {
  console.log('Élément double-cliqué');
});
  
```

**mousedown :** Se déclenche lorsque l'utilisateur appuie sur un bouton de la souris.

```js

document.getElementById('element').addEventListener('mousedown', function() {
  console.log('Bouton de la souris enfoncé');
});
  
```

**mouseup :** Se déclenche lorsque l'utilisateur relâche un bouton de la souris.

```js

document.getElementById('element').addEventListener('mouseup', function() {
  console.log('Bouton de la souris relâché');
});
  
```

**mouseenter :** Se déclenche lorsque la souris entre dans un élément.

```js

document.getElementById('element').addEventListener('mouseenter', function() {
  console.log('La souris entre dans l\'élément');
});
  
```

**mouseleave :** Se déclenche lorsque la souris quitte un élément.

```js

document.getElementById('element').addEventListener('mouseleave', function() {
  console.log('La souris quitte l\'élément');
});
  
```

**mousemove :** Se déclenche lorsque la souris se déplace à l'intérieur d'un élément.

```js

document.getElementById('element').addEventListener('mousemove', function() {
  console.log('La souris se déplace dans l\'élément');
});
  
```

**mouseover :** Se déclenche lorsque la souris survole un élément.

```js

document.getElementById('element').addEventListener('mouseover', function() {
  console.log('La souris survole l\'élément');
});
  
```

**mouseout :** Se déclenche lorsque la souris quitte un élément.

```js

document.getElementById('element').addEventListener('mouseout', function() {
  console.log('La souris quitte l\'élément');
});
  
```

### Événements liés au clavier

**keydown :** Se déclenche lorsqu'une touche est enfoncée.

```js

document.addEventListener('keydown', function() {
  console.log('Touche enfoncée');
});
  
```

**keyup :** Se déclenche lorsqu'une touche est relâchée.

```js

document.addEventListener('keyup', function() {
  console.log('Touche relâchée');
});
  
```

**keypress :** Se déclenche lorsqu'une touche est pressée et maintenue enfoncée.

```js

document.addEventListener('keypress', function() {
  console.log('Touche pressée');
});
  
```

### Événements liés au focus

**focus :** Se déclenche lorsqu'un élément reçoit le focus (entrée de texte, par exemple).

```js

document.getElementById('element').addEventListener('focus', function() {
  console.log('L\'élément reçoit le focus');
});
  
```

**blur :** Se déclenche lorsque l'élément perd le focus.

```js

document.getElementById('element').addEventListener('blur', function() {
  console.log('L\'élément perd le focus');
});
  
```

### Événements de formulaire

**submit :** Se déclenche lorsqu'un formulaire est soumis.

```js

document.getElementById('form').addEventListener('submit', function() {
  console.log('Formulaire soumis');
});
  
```

**change :** Se déclenche lorsqu'un élément de formulaire change de valeur.

```js

document.getElementById('input').addEventListener('change', function() {
  console.log('Valeur de l\'élément modifiée');
});
  
```

**input :** Se déclenche chaque fois que l'utilisateur entre des caractères dans un champ de saisie.

```js

document.getElementById('input').addEventListener('input', function() {
  console.log('Entrée de texte');
});
  
```

**focusin :** Se déclenche lorsque l'élément ou l'un de ses enfants reçoit le focus.

```js

document.getElementById('element').addEventListener('focusin', function() {
  console.log('Focus dans l\'élément ou ses enfants');
});
  
```

**focusout :** Se déclenche lorsque l'élément ou l'un de ses enfants perd le focus.

```js

document.getElementById('element').addEventListener('focusout', function() {
  console.log('Focus perdu dans l\'élément ou ses enfants');
});
  
```

### Événements de chargement

**load :** Se déclenche lorsque la page ou un élément (comme une image) a fini de se charger.

```js

window.addEventListener('load', function() {
  console.log('Page chargée');
});
  
```

**DOMContentLoaded :** Se déclenche lorsque le DOM est entièrement chargé.

```js

document.addEventListener('DOMContentLoaded', function() {
  console.log('DOM chargé');
});
  
```

**beforeunload :** Se déclenche avant que la page ne soit déchargée ou fermée.

```js

window.addEventListener('beforeunload', function() {
  console.log('Page va être déchargée');
});
  
```

**unload :** Se déclenche lorsque la page est déchargée.

```js

window.addEventListener('unload', function() {
  console.log('Page déchargée');
});
  
```

### Événements de la fenêtre

**resize :** Se déclenche lorsque la taille de la fenêtre change.

```js

window.addEventListener('resize', function() {
  console.log('Taille de la fenêtre modifiée');
});
  
```

**scroll :** Se déclenche lorsque l'utilisateur fait défiler la page.

```js

window.addEventListener('scroll', function() {
  console.log('Page défilée');
});
  
```

**orientationchange :** Se déclenche lorsque l'orientation de l'appareil change.

```js

window.addEventListener('orientationchange', function() {
  console.log('Orientation de l\'appareil modifiée');
});
  
```

### Événements tactiles

**touchstart :** Se déclenche lorsqu'un doigt touche l'écran.

```js

document.addEventListener('touchstart', function() {
  console.log('Toucher sur l\'écran');
});
  
```

**touchend :** Se déclenche lorsqu'un doigt quitte l'écran.

```js

document.addEventListener('touchend', function() {
  console.log('Doigt quitté l\'écran');
});
  
```

**touchmove :** Se déclenche lorsque le doigt se déplace sur l'écran.

```js

document.addEventListener('touchmove', function() {
  console.log('Doigt déplacé sur l\'écran');
});
  
```

**touchcancel :** Se déclenche lorsqu'une interaction tactile est annulée.

```js

document.addEventListener('touchcancel', function() {
  console.log('Interaction tactile annulée');
});
  
```

### Autres événements divers

**error :** Se déclenche lorsqu'une erreur se produit (par exemple, lors du chargement d'une image).

```js

window.addEventListener('error', function() {
  console.log('Erreur survenue');
});
  
```

**wheel :** Se déclenche lors du défilement avec la molette de la souris.

```js

document.addEventListener('wheel', function() {
  console.log('Molette de la souris utilisée');
});
  
```

**drag :** Se déclenche lorsqu'un élément est déplacé (glissé).

```js

document.addEventListener('drag', function() {
  console.log('Élément déplacé');
});
  
```

**dragstart :** Se déclenche lorsque l'élément commence à être déplacé.

```js

document.addEventListener('dragstart', function() {
  console.log('Déplacement commencé');
});
  
```

**dragend :** Se déclenche lorsque l'élément finit d'être déplacé.

```js

document.addEventListener('dragend', function() {
  console.log('Déplacement terminé');
});
  
```

**drop :** Se déclenche lorsqu'un élément est déposé après avoir été déplacé.

```js

document.addEventListener('drop', function() {
  console.log('Élément déposé');
});
  
```
