# v-for

v-for 用于数据循环, 多次渲染整个元素

遍历语法:

- v-for="(item, index) in 数组"

```html
<div id="app">
  <ul>
    <li v-for="(item, index) in list">{{ item }} - {{ index }}</li>
  </ul>
</div>
```

```js
const app = new Vue({
  el: '#app',
  data: {
    list: ['西瓜', '苹果', '香蕉']
  }
})
```

## v-for中的key

```html
<div id="app">
  <ul>
    <li v-for="(item, index) in books_list" :key="item.id">
      <span>{{ item.name }}</span>
      <span>{{ item.author }}</span>
      <button @click="del(item.id)">删除</button>
    </li>
  </ul>
</div>
```

```js
const app = new Vue({
  el: '#app',
  data: {
    books_list: [
      { id: 1, name: '西游记', author: '吴承恩' },
      { id: 2, name: '红楼梦', author: '曹雪芹' },
      { id: 3, name: '水浒传', author: '施耐庵' },
      { id: 4, neme: '三国演义', author: '罗贯中' }
    ]
  },
  methods: {
    del (id) {
      this.books_list = this.books_list.filter(item => item.id !== id)
    }
  }
})
```
