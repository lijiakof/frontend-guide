# Less 编码规范

Less 代码的基本规范和原则与[CSS 编码规范](./css.md)保持一致。

## 变量命名
*强制* 变量命名必须全字母小写，单词以 `-` 分隔。

示例：
```
// good
@nav-height: 88px;

// bad
@navHeight: 88px;
```

## 嵌套
*强制* 相关的样式，或者组件的样式，必须嵌套在同一个命名空间下。

示例：
```
// good
.nav {
  font-size: 18px;

  .nav-item {
    padding: 0 10px;
  }
}

// bad
.nav {
  font-size: 18px;
}

.nav .nav-item {
  padding: 0 10px;
}
```

## 继承
*强制* 使用继承时，如果声明块内使用`:extend`时，必须写在开头。

示例：
```
// good
.sub-nav {
  &:extend(.nav all);
  font-size: 16px;
}

// bad
.sub-nav {
  font-size: 16px;
  &:extend(.nav all);
}
```

## 混入（Mixin）

## 命名空间

## 注释