# v-html

v-html用于设置元素的innerHTML, 其值必须存在于Vue实例的data中

```html
<div id="app">
  <div v-html="msg"></div>
</div>
```

```js
const app = new Vue({
  el: '#app',
  data: {
    msg: `<h1>hello</h1>`
  }
})
```
