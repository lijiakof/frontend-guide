# 系统/项目架构

## 系统结构

![整体结构](../static/project-structure.png)

* 应用层：可扩展、可伸缩，具体某一个项目或者某个项目的子系统。
* 公共业务层：可扩展、可复用的业务级公共层，它是业务的抽象
* 框架层：可扩展、可复用的框架层，例如：`vue`、`react`、`lodash`、`moment` 等第三方框架及组建，也可以是团队长期积累的工具形成的框架。它是技术的沉淀和抽象。
* 运行环境：程序在`浏览器`、`Nodejs` 下运行，甚至可以是 `iOS` 和 `Android`。
* 持续集成：前端持续构建通常采用 `Webpack` 或者 `Rollup`，如果是 Apps 的构建我们通常采用 `xCode` 或者 `Maven`，当然我们不排除未来使用更先进的构建工具。

示例：

## 代码结构

示例：
```
.
├─envs
├─ src
│   ├─ apis
│   ├─ assets
│   ├─ business
│   ├─ components
│   ├─ layouts
│   ├─ middleware
│   ├─ pages
│   ├─ plugins
│   ├─ stores
│   ├─ types
│   └─ widgets
├─ static
├─ .env
├─ package.json
├─ README.md
└─ yarn.lock
```

* envs：不同环境的环境变量
* src：源代码
    * apis：和后端接口通讯的模块
    * assets：资源文件，将被编译到代码中去
    * business：公共业务层代码
    * components：业务级公共组件
    * layouts
    * middleware：中间件，在路由被调用时触发
    * pages：页面
    * plugins：框架级插件
    * stores：vuex
    * types
    * widgets：框架级组件
* static：静态资源文件，将被外部引用，可放入 CDN
* .env：环境变量文件
* package.json：项目文件
* README.md：项目帮助文档
* yarn.lock：管理项目的模块依赖

## 部署结构
// TODO

## 持续构建
// TODO