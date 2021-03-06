## 工程架构
- webpack配置
- node服务
- 服务端渲染基础

## 项目架构
- React
- React-Router配置
- Mobx配置
- 服务端渲染优化

## 业务开发
- 页面开发
- 登录服务
- 服务端渲染优化

## 项目部署
- PM2
- Nginx
- 一键部署

## 多页应用
- 内容都是由服务端用模版生成
- 每次页面跳转都要经过服务端
- JS更多只是处理动画
- 静态文件：使用gulp或grunt等工具手动编译到html中，自由度低，操作复杂，甚至不处理，直接交给后端，让后端服务处理

## 单页应用
- 所有内容都在前端生成
- JS承担更多的业务逻辑，后端只提供API
- 页面路由跳转不需要经过后端
- 类库：React、Vue、Angular、BackBone
- 架构工具：npm、bower、jspm
- 模块化工具：webpack、rollup、browserify
- 静态文件：可以直接在JS代码中进行引用，交由模块化工具转化成线上可用的静态资源，并且可以定制转化过程来适应不同的需求场景
- 其他：浏览器兼容性、toB还是toC、移动端还是PC端

## 常用配置
- webpack dev server
- Hot module replacement

## 使用eslint和editorconfig规范代码
- 规范代码有利用团队协作
- 纯手工规范费时费力而且不能保证准确性
- 能配合编辑自动提醒错误，提高开发效率
- eslint-config-airbnb
- babel-eslint
- eslint-config-standard
- eslint-loader
- eslint-plugin-import
- eslint-plugin-node
- eslint-plugin-jsx-ally
- eslint-plugin-promise
- eslint-plugin-react
- eslint-plugin-standard --save-dev

## 使用eslint强相关git绑定
- git init
- husky: commit前的校验

## 项目基本架构
- views：存放项目功能模块的页面，需要根据路由配置情况分割子级目录
- config：存放一些配置目录，比如第三方类库的引用，路由配置等
- store：存放项目store相关的文件，包括数据获取的封装等
- components：存放非业务组件，或者在多个业务间都需要用到的公用组件

## 什么是路由
- 路由是用来区分一个网站不同功能模块的地址，浏览器通过访问同一站点下的不同路由，来访问网站不同的功能。同样路由也让开发者区分返回的内容
- React-router 是一个非常好用的路由控制插件，能够让我们像书写jsx组件一样控制路由的跳转

## Mobx
- Mobx是flux实现的后起之秀，其以更简单的使用和更少的概念，让flux使用起来变得更加简单，相比redux有mutation、action、dispatch等概念，Mobx则更符合对store增删改查的操作概念

## 路由跳转
- 使用者可能从任意路由进入我们的网站，所以在服务端中也必须处理路由跳转，在返回给客户端的时候就是指定页面

## store数据同步
- 每个页面会有对应的数据，在服务端渲染时已经请求过对应数据，所以要让客户端知道这些数据，在客户端渲染的时候直接使用，而不是通过API再次请求，造成浪费
