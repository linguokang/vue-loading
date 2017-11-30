# vue-loading

> A Vue component to vue-loading 一个加载中弹窗插件

## 安装

``` bash
npm install vue-loading-easy -save
```

## SPA使用

```bash
import Loading from 'vue-loading-easy'

Vue.use(Loading)

// 作为组件的方式使用
<vue-loading :isLoading='true'></vue-loading>
```

## 直接引入使用

```bash

 <body>
    <div id="app"></div>

    <script src="./vue.min.js"></script>
    // 直接使用script导入
    <script src="./dist/vue-loading.js"></script>
    <script>
      var app1 = new Vue({
        el: '#app',
        data: {
          message: 'Hello Vue!'
        },
        template: `<div class="app">
                      <div class="app1"><vue-loading :isLoading="true" type="loading1" text="嘿嘿嘿" color="lightgreen" scale="1"></vue-loading></div>
                   </div>`
      })
    </script>
  </body>
```

## 配置

```bash
<vue-loading
   :isLoading='true'  //是否显示
   type="loading1"  //loading类型
   text="嘿嘿嘿" //加载文字
   color='lightgreen' //颜色
   scale='1'  //缩放倍数
</vue-loading>
```

### Props

| name          | Description  | type     | default  |
| ------------- |:------------:| -----:   |-----:|
| isLoading     | 是否显示      | Boolean  |false
| type          | 加载样式      | String   |loading1
| text          | 文字显示      | String   |加载中...
| color         | 图标颜色      | String   |lightgreen
| scale         | 弹窗缩放      | String   |1

