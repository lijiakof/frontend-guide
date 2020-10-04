# 文件命名规范
采用前端文件命名不成文的规定。

*强制* 文件/文件夹名单词必须全字母小写，单词以 `-` 分隔。

示例：
```
// good
src
 |-pages
    |-home.vue
    |-user-center.vue

// bad
Src
 |-pages
    |-Home.vue
    |-userCenter.vue
```

*强制* 文件有层次或者父子关系，用 `.` 分隔。

示例：
```
src
 |-pages
    |-home.vue
    |-home.banner.vue
    |-home.footer.vue
```

*建议* 文件夹名建议采用单词复数。