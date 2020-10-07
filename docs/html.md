# Html 编码规范

## 代码风格

### 缩进与换行
*强制* 使用 `2` 个`空格`为一个缩进层级。

示例：
```
<body>
  <div>
    <label>name: </label>
    <input
      type="text"
      name="name">
  </div>
</body>
```

*建议* 每行不得超过 `140` 个字符。

### 命名
*强制* `class` 样式名单词必须全字母小写，单词以 `-` 分隔。

示例：
```
<!-- good -->
<div class="hello-world">
  Hello world
</div>

<!-- bad -->
<div class="helloworld">
  Hello world
</div>
```

*强制* `id` 必须保证页面唯一，单词必须全字母小写，单词以 `-` 分隔。

示例：
```
<!-- good -->
<div id="hello-world">
  Hello world
</div>

<!-- bad -->
<div id="helloWorld">
  Hello world
</div>
```

### 注释
*强制* 必须独占一行。

示例：
```
<!-- good -->
<input type="text" />

<input type='text' /> <!-- bad -->
```

## 标签
*强制* 标签名必须使用小写字母。

示例：
```
<!-- good -->
<div>
  Hello world
</div>

<!-- bad -->
<DIV>
  Hello world
</DIV>
```

*强制* 必须闭合标签，对于无需自闭合的标签需要用 `/>` 闭合。

示例：
```
<!-- good -->
<input type="text" />
<div>hello</div>

<!-- bad -->
<input type="text">
<div>hello
```

*强制* 标签必须符合嵌套规则。

## 属性
*强制* 属性名必须使用小写字母，单词以 `-` 分隔。

示例：
```
<!-- good -->
<input
  type="text"
  v-model="name" />

<!-- bad -->
<input
  type="text"
  vModel="name" />
```

*强制* 属性值必须用双引号。

示例：
```
<!-- good -->
<input type="text" />

<!-- bad -->
<input type='text' />
<input type=text />
```

*强制* 多条属性必须换行。

示例：
```
<!-- good -->
<input
  type="text"
  placeholder="请输入"
  value="hello" />

<!-- bad -->
<input type="text" placeholder="请输入" value="hello" />
```

## head
*强制* 页面必须包含 title 标签声明标题。

示例：
```
<head>
  <meta charset="UTF-8">
  <title>标题</title>
</head>
```

*强制* 保证 favicon 可访问。

示例：
```
<head>
  <link
    rel="shortcut icon"
    href="path/to/favicon.ico">
</head>
```

*强制* 移动设备，必须指定页面的 viewport。
