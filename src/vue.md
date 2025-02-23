# vue基础

## 构建vue实例

```html
<div id="app">
  {{ msg }}
</div>
```

- {{ }}是插值表达式, 其中可以是被求值的代码, 使用的数据必须在Vue实例的data中, 不支持if、for等语句, 不能用作标签属性.

```js
const app = new Vue({
  el: '#app',
  data: {
    msg: 'Hello Vue'
  }
})
```

- 创建Vue实例, 通过` new Vue({}) `

- 指定配置项, 其中el是挂载点、data提供数据
