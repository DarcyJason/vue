# v-if

v-if用于控制元素显示隐藏(条件渲染), 不适用于频繁切换和隐藏的场景, 适用于基于条件判断, 进行创建或移除元素节点.

```html
<div id="app">
  <div v-if="flag">hello</div>
</div>
```

```js
const app = new Vue({
  el: '#app',
  data: {
    flag: true
  }
})
```
