# v-on

v-on 作用: 注册事件 = 添加监听 + 提供处理逻辑, 可以用@代替v-on:

语法: 
- v-on:事件名="内联语句"

- v-on:事件名="methods中的函数名"

## 语法一:

```html
<div id="app">
  <button v-on:click="count--"> - </button>
  <span>{{ count }}</span>
  <button @click="count++"> + </button>
</div>
```

```js
const app = new Vue({
  el: '#app',
  data: {
    count: 0
  }
})
```

## 语法二:

```html
<div id="app">
  <button @click="switch">切换显示或隐藏</button>
  <h1 v-show="flag">Hello Vue</h1>
</div>
```

```js
const app = new Vue({
  el: '#app',
  data: {
    flag: true
  },
  methods: {
    switch () {
      this.flag = !this.flag
    }
  }
})
```

## 调用传参

```html
<div id="app">
  <h1>售货机</h1>
  <button @click="buy(3)">可乐3元</button>
  <button @click="buy(4)">营养快线4元</button>
  <p>银行卡余额: {{ money }}元</p>
</div>
```

```js
const app = new Vue({
  el: '#app',
  data: {
    money: 100
  },
  methods: {
    buy (price) {
      this.money -= price
    }
  }
})
```
