# v-else和v-else-if

v-else 和 v-else-if 用于辅助 v-if 进行判断渲染

## v-else

```html
<div id="app">
  <p v-if="gender === 1">man</p>
  <p v-else>woman</p>
</div>
```

```js
const app = new Vue({
  el: '#app',
  data: {
    gender: 1
  }
})
```

## v-else-if

```html
<div id="app">
  <p v-if="score >= 90">优秀</p>
  <p v-else-if="score >= 80">良好</p>
  <p v-else-if="score >= 60">及格</p>
  <p v-else>不及格</p>
</div>
```

```js
const app = new Vue({
  el: '#app',
  data: {
    score: 80
  }
})
```
