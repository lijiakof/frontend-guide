# 文件命名规范
采用前端文件命名不成文的规定，我们可以参考各种前端项目，babel、vue、apollo，它们项目的文件以及文件夹都是小写字母，并且单词以 `-` 分隔；另外我们还参考 RESTful 的风格，每个文件或者文件夹都是一个或者多个资源，尽量采用名词来命名。

*强制* 文件/文件夹名单词必须全字母小写，单词以 `-` 分隔。

示例：
```
// good
.
└─ src
    ├─ assets
    │   ├─ default.less
    │   └─ reset-style.less
    └─ pages
        ├─ home.vue
        └─ user-center.vue

// bad
.
└─ Src
    ├─ assets
    └─ pages
        ├─ Home.vue
        └─ userCenter.vue
```

*强制* 文件有层次或者父子关系，用 `.` 分隔。

示例：
```
.
└─ src
    └─ pages
        ├─ home.vue
        ├─ home.banner.vue
        └─ home.footer.vue
```

*建议* 文件夹名建议采用单词复数。

示例：
```
// good
.
└─ src
    ├─ components
    ├─ pages
    └─ plugins

// bad
.
└─ src
    ├─ component
    ├─ page
    └─ plugin
```