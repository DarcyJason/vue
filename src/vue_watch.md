# watch属性

```html
<div class="app">
  <div class="box">
    <div class="input-wrap">
      <textarea v-model="words"></textarea>
    </div>
    <div class="output-wrap">
      <div class="transbox">{{ result }}</div>
    </div>
  </div>
</div>
```

```js
const app = new Vue({
  el: '#app',
  data: {
    words: '',
    result: '',
  },
  watch: {
    // 一般不用old_value, 可以省略
    words (new_value, old_value) {
      clearTimeout(this.timer)
      this.timer = setTimeout(async () => {
        const res = await axios({
          url: 'https://backendapi',
          params: {
            words: new_value
          }
        })
        this.result = res.data.data
      }, 200)
    }
  }
})
```

## 完整写法

```html
<div class="app">
  <div class="query">
    <span>翻译成语言: </span>
    <select v-model="lang">
      <option value="italy">意大利</option>
      <option value="english">英语</option>
      <option value="german">德语</option>
    </select>
  </div>
  <div class="box">
    <div class="input-wrap">
      <textarea v-model="words"></textarea>
    </div>
    <div class="output-wrap">
      <div class="transbox">{{ result }}</div>
    </div>
  </div>
</div>
```

```js
const app = new Vue({
  el: '#app',
  data: {
    obj: {
      words: '',
      lang: 'italy',
    },
    result: '',
  },
  watch: {
    obj: {
      deep: true, // 深度监视
      immediate: true, // 立刻执行, 一进入页面立刻执行handler函数一次
      handler (new_value) {
        clearTimeout(this.timer)
        this.timer = setTimeout(async () => {
          const res = await axios({
            url: 'https://backendapi',
            params: new_value
          })
          this.result = res.data.data
        }, 200)
      }
    }
  }
})
```
