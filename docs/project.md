# 系统/项目架构

## 系统结构
* 应用层
* 公共业务层
* 框架层
* 运行环境

## 代码结构

示例：
```
.
├──envs
├── src
│   ├── apis
│   ├── assets
│   ├── business
│   ├── components
│   ├── layouts
│   ├── middleware
│   ├── pages
│   ├── plugins
│   ├── stores
│   ├── types
│   └── widgets
├── static
├── .env
├── package.json
├── README.md
└── yarn.lock
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