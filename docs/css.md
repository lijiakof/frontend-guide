# Css 编码规范

## 代码风格

### 缩进
*强制* 使用 `2` 个`空格`为一个缩进层级。

示例：
```
.title {
  font-size: 20px;
  color: #ccc;
}
```

### 空格
*强制* `选择器` 与 `{` 之间必须包含空格。

示例：
```
/* good */
.title {
  font-size: 20px;
}

/* bad */
.title{
  font-size: 20px;
}
```

*强制* `属性名` 与之后的 `:` 之间不允许包含空格，`:` 与 `属性值` 之间必须包含空格。

示例：
```
/* good */
.title {
  font-size: 20px;
}

/* bad */
.title {
  font-size :20px;
}
.title {
  font-size:20px;
}
```

*强制* 列表型属性值书写在单行时，`,` 后必须跟一个空格。

示例：
```
/* good */
.title {
  font-family: Arial, sans-serif;
}

/* bad */
.title {
  font-family: Arial,sans-serif;
}
```

### 命名
*强制* 样式名单词必须全字母小写，单词以 `-` 分隔。

示例：
```
/* good */
.nav-bar {
  font-size: 24px;
}

/* bad */
.navBar {
  font-size: 24px;
}
.NavBar {
  font-size: 24px;
}
```

### 注释

## 选择器
*强制* 当一个样式规则中包含多个选择器时，每个选择器声明必须独占一行。

示例：
```
/* good */
body,
html,
page {
  font-size: 12px;
}

/* bad */
body, html, page {
  font-size: 12px;
}
```

*强制* `>`、`+`、`~` 选择器的两边各保留一个空格。

示例：
```
/* good */
body > page {
  font-size: 12px;
}

/* bad */
body>page {
  font-size: 12px;
}
```

*强制* 属性选择器中的值必须使用`双引号`。

示例：
```
/* good */
input[type="text"] {
  font-size: 12px;
}

/* bad */
input[type='text'] {
  font-size: 12px;
}
```

## 属性
*强制* 属性定义必须另起一行。

*强制* 属性定义后必须以分号结尾。

*建议* 属性在书写时，应按功能进行分组，并以 Formatting Model > Box Model > Typographic > Visual 的顺序书写，以提高代码的可读性。

* Positioning Model 布局方式、位置，相关属性包括：position, top, z-index, display, float等
* Box Model 盒模型，相关属性包括：width, height, padding, margin，border,overflow
* Typographic 文本排版，相关属性包括：font, line-height, text-align
* Visual 视觉外观，相关属性包括：color, background, list-style, transform, animation

## z-index

## 值与单位
*强制* 文本内容必须用双引号包围。
*强制* url() 函数中的路径不加引号。
*强制* RGB颜色值必须使用十六进制记号形式 #rrggbb。不允许使用 rgb()。
*强制* 颜色值不允许使用命名色值。