# v-model

v-model 用于给表单元素进行双向绑定, 可以快速获取表单元素的值

```html
<div id="app">
  账户: <input type="text" v-model="username"> <br><br>
  密码: <input type="password" v-model="password">
  <button>登录</button>
  <button>重置</button>
</div>
```

```js
const app = new Vue({
  el: '#app',
  data: {
    username: '',
    password: '',
  },
  methods: {
    login () {
      console.log(this.username, this.password)
    },
    reset () {
      this.username = ''
      this.password = ''
    }
  }
})
```

## 复选框

```html
<div id="app">
  是否单身: <input type="checkbox" v-model="is_single">
</div>
```

```js
const app = new Vue({
  el: '#app',
  data: {
    is_single: true
  }
})
```

## 单选框

```html
<div id="app">
  性别:
  <input v-model="gender" type="radio" name="gender" value="1">男
  <input v-model="gender" type="radio" name="gender" value="0">女
</div>
```

```js
const app = new Vue({
  el: '#app',
  data: {
    gender: "1"
  }
})
```

## 下拉菜单

```html
<div id="app">
  所在城市
  <select v-model="city_id">
    <option value="101">北京</option>
    <option value="102">上海</option>
    <option value="103">成都</option>
    <option value="104">南京</option>
  </select>
</div>
```

```js
const app = new Vue({
  el: '#app',
  data: {
    city_id: '101'
  }
})
```

## 文本框

```html
<div id="app">
  自我描述:
  <textarea v-model="description"></textarea>
</div>
```

```js
const app = new Vue({
  el: '#app',
  data: {
    description: ""
  }
})
```
