# Vue生命周期

## 一、生命周期
一个Vue实例从创建到销毁的整个过程

## 二、生命周期的四个阶段
1. 创建
2. 挂载
3. 更新
4. 销毁

## 三、生命周期钩子函数
生命周期钩子函数是vue生命过程中会自动执行的函数, 可以在生命周期钩子函数中嵌入自己的代码逻辑, 一般最常用的是created、 mounted函数
- 创建阶段: beforeCreate、 created
- 挂载阶段: beforeMount、 mounted
- 更新阶段: beforeUpdate、 updated
- 销毁阶段: beforeDestory、 destroyed

```js
const app = new Vue({
  el: '#app',
  data: {

  },
  beforeCreate () {},
  created () {},
  beforeMount () {},
  mounted () {},
  beforeUpdate () {},
  updated () {},
  beforeDestory () {},
  destroyed () {}
})
```
