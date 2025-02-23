# v-show

v-show用于控制元素的显示于隐藏, 适用于频繁切换和隐藏的场景

```html
<div id="app">
  <div v-show="flag">hello</div>
</div>
```

```js
const app = new Vue({
  el: '#app',
  data: {
    flag: false
  }
})
```
