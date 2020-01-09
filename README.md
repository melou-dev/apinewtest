# CONSOMMER UNE API with AXIOS

https://fr.vuejs.org/v2/cookbook/using-axios-to-consume-apis.html
https://github.com/axios/axios
https://api.coindesk.com/v1/bpi/currentprice.json

Ci-dessous, des questions que je me suis posée.

## Rappel HTML

<span> est très proche de l'élément <div>, mais l'élément <div> est un élément de bloc,
alors que <span> est un élément en ligne.

## Dans Js <Script>

Après avoir installer AXIOS ne pas oublié de mettre le code suivant pour appliquer axios
`import axios from "axios";`

`new Vue` vs `export default`
**New vue** : l s'agit généralement de votre instance Vue racine à partir de laquelle le reste
de l'application descend. Il est lié à l'élément racine déclaré dans un document html,
par exemple:

```
<html>
  ...
  <body>
    <div id="app"></div>
  </body>
</html>
```

```
new Vue({
    el: '#app', //el pour "élément", # pour id
    data () {
      return {}
    }
)}
```

La syntaxe **export default** déclare un composant qui peut être enregistré et réutilisé ultérieurement.
Par exemple, si vous créez un composant de fichier unique comme:

```
// my-component.js
export default {
    name: 'my-component',
    data () {
      return {}
    }
}
```

## Consernant la directive vue.js v-for.

Afin que les éléments existants puissent être réutilisés et réordonnés,
vous devez fournir un attribut unique key pour chaque élément :

`<div v-else v-for="currency in info" class="currency" :key="currency.id">`
