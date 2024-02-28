# JSYG.Editor
Editor of svg shapes with [JSYG framework](https://github.com/YannickBochatay/JSYG)

If you look for a complete SVG editor with very simple API, try [JSYG.FullEditor](https://github.com/YannickBochatay/JSYG.FullEditor).
This one is just a brick.


### Demo
[http://yannickbochatay.github.io/JSYG.Editor/](http://yannickbochatay.github.io/JSYG.Editor/)


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
