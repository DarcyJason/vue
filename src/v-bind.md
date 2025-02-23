# v-bind

v-bind 用于动态设置html的标签属性, 可以用:代替v-bind:

语法:

- v-bind:属性值="表达式"

## v-bind 完整写法
```html
<div id="app">
  <img v-bind:src="img_url" alt="">
</div>
```

```js
const app = new Vue({
  el: '#app',
  data: {
    img_url: './img.jpg'
  }
})
```

## v-bind 简单写法
```html
<div id="app">
  <img :src="img_url" alt="">
</div>
```

```js
const app = new Vue({
  el: '#app',
  data: {
    img_url: './img.jpg'
  }
})
```

## v-bind 控制样式

```html
<div class="box" :style="{ css属性名1: css属性值1, css属性名2: css属性值2}"></div>
```
