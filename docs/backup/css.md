# Css 编码规范

### **✊🏻强制** 使用 `2` 个`空格`为一个缩进层级。

示例：
```css
.title {
  font-size: 20px;
  color: #ccc;
}
```

### **✊🏻强制** `选择器` 与 `{` 之间必须包含空格。

示例：
```css
/* 👍🏻 good */
.title {
  font-size: 20px;
}

/* 👎🏻 bad */
.title{
  font-size: 20px;
}
```

### **✊🏻强制** `属性名` 与之后的 `:` 之间不允许包含空格，`:` 与 `属性值` 之间必须包含空格。

示例：
```css
/* 👍🏻 good */
.title {
  font-size: 20px;
}

/* 👎🏻 bad */
.title {
  font-size :20px;
}
.title {
  font-size:20px;
}
```

### **✊🏻强制** 列表型属性值书写在单行时，`,` 后必须跟一个空格。

示例：
```css
/* 👍🏻 good */
.title {
  font-family: Arial, sans-serif;
}

/* 👎🏻 bad */
.title {
  font-family: Arial,sans-serif;
}
```

### **✊🏻强制** 样式名单词必须全字母小写，单词以 `-` 分隔。

示例：
```css
/* 👍🏻 good */
.nav-bar {
  font-size: 24px;
}

/* 👎🏻 bad */
.navBar {
  font-size: 24px;
}
.NavBar {
  font-size: 24px;
}
```

### 注释
TODO:

### **✊🏻强制** 当一个样式规则中包含多个选择器时，每个选择器声明必须独占一行。

示例：
```css
/* 👍🏻 good */
body,
html,
page {
  font-size: 12px;
}

/* 👎🏻 bad */
body, html, page {
  font-size: 12px;
}
```

### **✊🏻强制** `>`、`+`、`~` 选择器的两边各保留一个空格。

示例：
```css
/* 👍🏻 good */
body > page {
  font-size: 12px;
}

/* 👎🏻 bad */
body>page {
  font-size: 12px;
}
```

### **✊🏻强制** 属性选择器中的值必须使用`双引号`。

示例：
```css
/* 👍🏻 good */
input[type="text"] {
  font-size: 12px;
}

/* 👎🏻 bad */
input[type='text'] {
  font-size: 12px;
}
```

### **✊🏻强制** 属性定义必须另起一行。

示例：
```css
/* 👍🏻 good */
.title {
  font-size: 20px;
  line-height: 1.5;
  color: #ccc;
}

/* 👎🏻 bad */
.title {
  font-size: 20px; line-height: 1.5; color: #ccc;
}
```

### **✊🏻强制** 属性定义后必须以分号结尾。

示例：
```css
/* 👍🏻 good */
.title {
  font-size: 20px;
}

/* 👎🏻 bad */
.title {
  font-size: 20px
}
```

### **🙏🏻建议** 属性在书写时，应按功能进行分组，并以 Formatting Model > Box Model > Typographic > Visual 的顺序书写，以提高代码的可读性。

* Positioning Model 布局方式、位置，相关属性包括：position, top, z-index, display, float等
* Box Model 盒模型，相关属性包括：width, height, padding, margin，border,overflow
* Typographic 文本排版，相关属性包括：font, line-height, text-align
* Visual 视觉外观，相关属性包括：color, background, list-style, transform, animation

示例：
```css
.tool-bar {
  /* formatting model */
  position: absolute;
  top: 50px;
  right: 20px;

  /* box model */
  width: 40px;
  padding: 40px;
  border: 1px solid #ccc;

  /* typographic */
  font-size: 12px;

  /* visual */
  color: #333;
  background-color: #fff;
}
```

### z-index
TODO:

### **✊🏻强制** 文本内容必须用双引号包围。

### **✊🏻强制** url() 函数中的路径不加引号。

示例：
```css
/* 👍🏻 good */
.banner {
  background: url(/images/bg.png);
  
}

/* 👎🏻 bad */
.banner {
  background: url("/images/bg.png");
  
}
```

### **✊🏻强制** RGB颜色值必须使用十六进制记号形式 #rrggbb。不允许使用 rgb()。

示例：
```css
/* 👍🏻 good */
.title {
  color: #000;
  
}

/* 👎🏻 bad */
.title {
  color: rgb(0, 0, 0);
}
```

### **✊🏻强制** 颜色值不允许使用命名色值。

示例：
```css
/* 👍🏻 good */
.title {
  color: #000;
  
}

/* 👎🏻 bad */
.title {
  color: black;
}
```