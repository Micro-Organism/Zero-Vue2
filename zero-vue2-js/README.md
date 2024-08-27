<h1>Zero-Vue2</h1>

# 1.简介
```
基于Vue2 + ElementUI + Vue Router + Vuex + Axios + ECharts的通用后台管理系统模板，
支持多主题切换，支持多语言切换，支持自定义主题颜色，支持自定义主题字体，
支持自定义主题布局，支持自定义主题菜单，支持自定义主题表格，支持自定义主题图表，
支持自定义主题表单，支持自定义主题按钮，支持自定义主题图标，支持自定义主题图片，
```

# 2.目录结构
```
├── src // 源代码
│   ├── assets // 静态资源
│   ├── components // 公共组件
│   ├── config // 配置文件
│   ├── icons // 图标
│   ├── layout // 布局
│   ├── router // 路由
│   ├── store // 状态管理
│   ├── utils // 工具类
│   ├── views // 页面
│   ├── App.vue // 根组件
│   ├── main.js // 入口文件
│   ├── permission.js // 权限控制
│   ├── settings.js // 配置文件
│   └── store.js // 状态管理
├── public // 公共资源
│   ├── index.html // 入口文件
├── .babelrc // babel配置文件
├── .eslintrc.js // eslint配置文件
├── .gitignore // git忽略文件
├── .postcssrc.js // postcss配置文件
├── package.json // 项目配置文件
└── README.md // 项目说明文件
```

# 安装
```
1. 克隆项目到本地
2. 安装依赖
   npm install
3. 运行项目
   npm run dev
4. 打包项目
   npm run build
```

# 3.技术栈

## 3.1.Vue2
```
Vue2是一个渐进式JavaScript框架，用于构建用户界面。它提供了响应式数据绑定和组件化开发的能力，使得开发者可以更加高效地构建复杂的用户界面。
```

## 3.2.ElementUI
### 3.2.1.简介
```
ElementUI是一个基于Vue2的UI组件库，提供了丰富的UI组件，如按钮、表单、表格、对话框等，帮助开发者快速构建高质量的用户界面。
```
### 3.2.2.设计原则
```
1. 一致性 Consistency
2. 反馈 Feedback
3. 效率 Efficiency
3. 可控 Controllability
```
### 3.2.3.特点
```
1. 基于Vue2，支持Vue2的所有特性
2. 提供丰富的UI组件，满足各种需求
3. 支持自定义主题，可以自定义主题颜色、字体、布局等
4. 支持多语言，可以切换中英文等
5. 支持响应式布局，可以适配各种屏幕尺寸
6. 支持国际化，可以切换语言等
7. 支持按需加载，可以只引入需要的组件
8. 支持自定义图标，可以自定义图标样式等
9. 支持自定义表单验证，可以自定义表单验证规则等
10. 支持自定义表格，可以自定义表格样式等
11. 支持自定义对话框，可以自定义对话框样式等
12. 支持自定义按钮，可以自定义按钮样式等
13. 支持自定义图标，可以自定义图标样式等
14. 支持自定义图片，可以自定义图片样式等
```
### 3.2.4.使用
#### 安装
```shell
### 安装element-ui
   npm install element-ui --save
### 安装sass-loader和node-sass
   npm install sass-loader node-sass --save-dev
### cdn
   <link rel="stylesheet" href="https://unpkg.com/element-ui/lib/theme-chalk/index.css">
   <script src="https://unpkg.com/vue/dist/vue.js"></script>
```   
#### 引入
```typescript
import Vue from 'vue';
import ElementUI from 'element-ui';
import 'element-ui/lib/theme-chalk/index.css';
Vue.use(ElementUI);

new Vue({
  el: '#app',
  render: h => h(App)
});
```
#### 导航
```
导航可以解决用户在访问页面时：在哪里，去哪里，怎样去的问题。一般导航会有「侧栏导航」和「顶部导航」2 种类型。
```
##### 侧栏导航
```
侧栏导航是左侧的导航菜单，可将导航栏固定在左侧，提高导航可见性，方便页面之间切换；
顶部可放置常用工具，如搜索条、帮助按钮、通知按钮等。适用于中后台的管理型、工具型网站。
1.一级类目
适用于结构简单的网站：只有一级页面时，不需要使用面包屑。
2.二级类目
侧栏中最多可显示两级导航；当使用二级导航时，我们建议搭配使用面包屑，方便用户定位自己的位置和快速返回。
3.三级类目
适用于较复杂的工具型后台，左侧栏为一级导航，中间栏可显示其对应的二级导航，也可放置其他的工具型选项。
```
##### 顶部导航
```
顶部导航是顶部的导航菜单，顺应了从上至下的正常浏览顺序，方便浏览信息；
顶部宽度限制了导航的数量和文本长度。
适用于导航较少，页面篇幅较长的网站。
```
#### 自定义主题

#### 内置过渡动画
1. fade 淡入淡出
```vue
<template>
  <div>
    <el-button @click="show = !show">Click Me</el-button>
    <transition name="el-fade-in-linear">
      <div v-if="show">el-fade-in-linear</div>
    </transition>
    <transition name="el-fade-in">
      <div v-show="show">.el-fade-in</div>
    </transition>
  </div>
</template>

<script>
export default {
  data: ()=>({
    show: true
  })
}
</script>
```
2. zoom 缩放
```vue
<template>
  <div>
    <el-button @click="show = !show">Click Me</el-button>
    <transition name="el-zoom-in-center">
      <div v-if="show">el-zoom-in-center</div>
    </transition>
    <transition name="el-zoom-in-top">
      <div v-if="show">el-zoom-in-top</div>
    </transition>
    <transition name="el-zoom-in-bottom">
      <div v-if="show">el-zoom-in-bottom</div>
    </transition>
  </div>
</template>
<script>
export default {
  data: ()=>({
    show: true
  })
}
</script>
```
3. collapse 折叠
```vue
<template>
  <div>
    <el-button @click="show = !show">Click Me</el-button>
    <el-collapse-transition>
      <div v-show="show">
        <div>el-collapse-transition</div>
        <div>el-collapse-transition</div>
      </div>
    </el-collapse-transition>
  </div>
</template>
<script>
export default {
  data: () => ({
    show: true
  })
}
</script>
```
4. slide 滑动
3. bounce 弹跳

#### 多语言

#### 响应式布局

#### 国际化

#### 按需加载

#### 自定义图标

#### 自定义表单验证

#### 自定义表格

#### 自定义对话框

#### 自定义按钮

#### 自定义图标

#### 自定义图片

#### 其他功能

## 3.3.Vue Router
```
Vue Router是一个基于Vue2的路由管理器，用于管理单页面应用程序的路由。它提供了路由守卫、路由懒加载等功能，使得开发者可以更加灵活地管理应用程序的路由。
```

## 3.4.Vuex
```
Vuex是一个基于Vue2的状态管理库，用于管理应用程序的状态。它提供了集中式存储、状态变更跟踪、状态持久化等功能，使得开发者可以更加方便地管理应用程序的状态。
```

## 3.5.Axios
```
Axios是一个基于Promise的HTTP客户端，用于发送HTTP请求。它提供了拦截器、取消请求、自动转换JSON等功能，使得开发者可以更加方便地发送HTTP请求。
```

## 3.6.ECharts
```
ECharts是一个基于JavaScript的开源可视化图表库，提供了丰富的图表类型，如折线图、柱状图、饼图、散点图等，可以帮助开发者快速构建高质量的图表。
```

## 3.7.其他
```
除了上述技术栈外，还使用了其他一些技术，如less、sass、postcss、eslint、babel等。
```

# 功能
```
1. 登录/注销
2. 首页
3. 用户管理
4. 角色管理
5. 菜单管理
6. 部门管理
7. 字典管理
8. 操作日志
9. 登录日志
10. 通知公告
11. 代码生成
12. 系统监控
13. 个人中心
14. 其他功能
```

# 使用
```
1. 登录
   输入用户名和密码，点击登录按钮
2. 首页
   首页展示系统信息，包括系统名称、版本号、版权信息等
3. 用户管理
   用户管理展示用户列表，包括用户名、昵称、性别、邮箱、手机号、状态、创建时间、操作等
4. 角色管理
   角色管理展示角色列表，包括角色名称、角色描述、状态、创建时间、操作等
5. 菜单管理
   菜单管理展示菜单列表，包括菜单名称、菜单路径、菜单图标、菜单状态、创建时间、操作等
6. 部门管理
   部门管理展示部门列表，包括部门名称、部门描述、状态、创建时间、操作等
7. 字典管理
   字典管理展示字典列表，包括字典名称、字典类型、字典值、字典标签、状态、创建时间、操作等
8. 操作日志
   操作日志展示操作日志列表，包括操作用户、操作类型、操作时间、操作IP、操作结果、操作详情等
9. 登录日志
   登录日志展示登录日志列表，包括登录用户、登录时间、登录IP、登录结果、登录详情等
10. 通知公告
   通知公告展示通知公告列表，包括公告标题、公告内容、公告类型、公告状态、创建时间、操作等
11. 代码生成
   代码生成展示代码生成列表，包括生成模板、生成路径、生成时间、操作等
12. 系统监控
   系统监控展示系统监控信息，包括CPU使用率、内存使用率、磁盘使用率、网络使用率等
13. 个人中心
   个人中心展示个人信息，包括用户名、昵称、性别、邮箱、手机号、头像、操作等
14. 其他功能
   其他功能展示其他功能列表，包括功能名称、功能描述、功能状态、创建时间、操作等
```