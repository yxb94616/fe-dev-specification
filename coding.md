# 规范不是规定，只是一种风格

## 常用编码规范

### html 代码编写规范

1. 使用语义化标签如 section footer header 进行布局页面结构
2. 使用标准 html5 文档类型声明
3. 使用 utf-8 编码 `<meta charset="utf-8">`
4. 尽量使用比较少的标签
5. 使用尽量贴合语意，如，布局容器使用 div，段落使用 p。数据列表使用 ul/ol/dd 等，关键字使用 strong，标题使用 h1~h6，图标使用 i；

### 样式 class 命名规范

1. 参与到 ui 交互的 class 使用前缀 js-的命名规则，与定义样式的 class 区别开
2. 参与布局的 class 使用前缀 ly- （layout 简称）
3. 全局 class 使用前缀 g-
4. 对页面和组件统一命名，如页面需要添加 class=”page-页面名” 组件添加 class=”component-组件名”进行区分
5. 取名尽量贴合语意 （使用翻译软件翻译下）
6. 页面须有一个私有的 class 选择器空间 scoped

### js 代码编写规范

1. 使用统一缩进，以 tab 缩进，一个 tab 大小为 2 个空格
2. 函数/方法，要添加功能注释
3. 函数/方法要保持功能单一，一个方法只做一件事情，复杂的功能要进行拆分
4. 来自于接口返回的数据，和来自于本地存储的数据使用之前要做容错处理，保证程序健壮性
5. 该用 switch 的时候用 switch，滥用 if/else 会使程序的可读性变差
6. 在一票否决的情况下，可以采用写法如 if(x)return 减少代码块嵌套深度

### IE 兼容模式

1. 优先使用最新版本的 IE 和 Chrome 内核

```html
<meta http-equiv="X-UA-Compatible" content="IE=edge,chrome=1" />
```

### 移动端样式书写规范

1. 尽可能使用以屏幕宽度为参照的等比例布局 以 js 根据屏幕宽度动态计算根元素 font-size 变换 rem 与 px 换算比例，做到等比缩放
2. 定义 viewport 为移动端设备优化，设置可见区域的宽度和初始缩放比例,禁止用户手动缩放

```html
<meta
  name="viewport"
  content="width=device-width, initial-scale=1.0, maximum-scale=1.0, user-scalable=0"
/>
```

### 常用库、插件建议

1. jquery
2. swiper
3. layui  

  欢迎补充你认为的好用的轮子，避免造轮子

## vue 项目目录结构规范

### 1、以 vue-cli3 创建项目

1. 项目名尽量与后台名称一致
2. 选择手动配置项目功能
3. 功能选择必须包含：Babel、Router、Vuex、CSS Pre-processors、Linter/Formatter
4. 将插件的配置保存在各自的配置文件 (比如 '.babelrc') 中
5. 默认 hash 路由
6. 建议选择 css 预处理器为 Sass/SCSS (with dart-sass)
7. 建议语法规则和代码风格的检查使用 ESLint + Prettier

### 2、修改目录如下

public `该目录下除index.html文件，其余资源在打包的时候不会被编译`  
src `该目录所有资源都会被编译打包`  
|—— api `接口定义目录 （http.js定义axios封装和公共路径配置）`  
|—— assets `静态文件目录`  
|—— components `公共组件目录 （可将查询，表格，分页或者布局类的组件封装为公共组件）`  
|—— directives `全局自定义指令`  
|—— filter `全局过滤器`  
|—— plugins `第三方插件`  
|—— router `路由定义`  
|—— store `状态管理定义`  
|—— styles `样式`  
|—— utils `工具库`  
|—— views `页面`  

等等，根据需求再添加新的

### vue 项目规范

1. Vue 项目编码规范建议阅读官方网站 [风格指南](https://cn.vuejs.org/v2/style-guide/ "风格指南")
2. Vue 常用 UI 库选择建议 Element > iView > Ant Design Vue

### vue 常用插件

1. babel-polyfill
2. axios （http 库）
3. v-viewer （图片查看器）
4. vue-lazyload （图片懒加载）
5. vxe-table （表格）
6. xe-utils （工具库，vxe-table 正好也需要依赖这个库）  
欢迎补充实用的、稳定的、好用的Vue插件
