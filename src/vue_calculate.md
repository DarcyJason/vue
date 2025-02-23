# 计算属性

```html
<div id="app">
  <table>
    <tr>
      <th>名字</th>
      <th>数量</th>
    </tr>
    <tr v-for="(item, index) in list" :key="item.id">
      <td>{{ item.name }}</td>
      <td>{{ item.num}}</td>
    </tr>
  </table> 
  <p>礼物总数: {{ total_count }} 个</p>
</div>
```

```js
const app = new Vue({
  el: '#app',
  data: {
    list: [
      { id: 1, name: '篮球', num: 1 },
      { id: 2, name: '玩具', num: 2 },
      { id: 3, name: '铅笔', num: 3 }
    ]
  },
  computed: {
    total_count () {
      let total = this.list.reduce((sum, item) => sum + item.num, 0)
      return total
    }
  }
})
```

## 完整写法

```html
<div id="app">
  姓: <input type="text" v-model="first_name"> +
  名: <input type="text" v-model="last_name"> = 
  <span>{{ full_name }}</span>
  <button @click="change_name">改名</button>
</div>
```

```js
const app = new Vue({
  el: '#app',
  data: {
    first_name: '',
    last_name: '',
  },
  methods: {
    change_name () {
      this.name = "牛逼"
    }
  },
  computed: {
    full_name: {
      get() {
        return this.first_name + this.last_name
      },
      set(value) {
        this.first_name = value.slice(0, 1)
        this.last_name = value.slice(1)
      }
    }
  }
})
```
