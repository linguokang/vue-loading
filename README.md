# vue-loading

> A Vue component to pay-keyboard 一个加载中弹窗插件

## 安装

``` bash
npm install vue-loading-easy -save
```

## 使用

```bash
import Loading from 'vue-loading-easy'

Vue.use(Loading)

// 或者直接使用script导入
<script src="./node_modules/vue/dist/vue-loading.js"></script>

// 作为组件的方式使用
<vue-loading :isLoading='true'></vue-loading>
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

