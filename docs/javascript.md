# JavaScript 编码规范

## 代码风格

### 缩进与换行
*强制* 使用 `2` 个`空格`为一个缩进层级。

示例：
```javascript
function fun () {
  console.log('Hello world!');
}
```

*强制* 每个独立语句结束后必须换行。

*建议* 每行不得超过 `140` 个字符。

### 空格
*强制* `二元运算符`两侧必须有一个空格，`一元运算符`与操作对象之间不允许有空格。

示例：
```javascript
let a = 1;
a++;
a = b + c;
```

*强制* 用作代码块起始的左 `{` 前必须有一个空格。

示例：
```javascript
// good
if (a) {
  // ...
}
for (i = 0; i < 10; i++) {
  // ...
}

// bad
if (a){
  // ...
}
for (i = 0; i < 10; i++){
  // ...
}
```

*强制* 在对象创建时，属性中的 `:` 之后必须有空格，`:` 之前不允许有空格。

示例：
```javascript
// good
let obj = {
  name: 'jay',
  title: 'Hello'
};

// bad
let obj = {
  name:'jay',
  title :'Hello'
};
```

*强制* 函数声明、具名函数表达式、函数调用中，函数名和 `(` 之间必须有空格。
// TODO

*强制* `,` 和 `;` 前不允许有空格。如果不位于行尾，`,` 和 `;` 后必须跟一个空格。

示例：
```javascript
// good
function fn (name, title) {
  // ...
}
fn('jay', 'Hello');

// bad
function fn (name,title) {
  // ...
}
fn('jay','Hello');
```

*强制* 单行声明的数组与对象，如果包含元素，`{}` 和 `[]` 内紧贴括号部分必须包含空格。
// TODO

### 命名
*强制* 常量全部大写，单词以 `_` 分隔。

示例：
```javascript
const USER_NAME = 'jay';
```

*强制* 变量、函数、参数、属性采用`小驼峰`命名法。

示例：
```javascript
let userName = 'jay';
```

*强制* 类名采用`大驼峰`命名法。

示例：
```javascript
class User {
  // ...
}
```

*强制* 类名采用`名词`。

*建议* 函数名采用`动名词`。

*建议* Boolean 类型的变量使用 `is` 或者 `has` 开头。

## 文档化注释
采用文档化注释的好处，规范的注释，一键生成文档，我们在框架级别的代码中使用的最多。https://jsdoc.app/

* *强制* @module 定义模块
* *强制* @class 定义类
* *强制* @constructor 定义构造函数
* *强制* @param 入参
* *强制* @return 返回值
* *强制* 单行注释必须独占一行。
* 参考：https://jsdoc.app/ https://github.com/jsdoc/jsdoc

示例：
```javascript
/**
 * Customer
 * https://github.com/thetripio/tripio-js/blob/master/src/room-night/customer.js
 * @class
 */
export default class Customer {
  constructor () {

  }

  /**
    * Get all the room nights of the msg.sender(Customer or Vendor)
    * @param {Number} from - The begin id, if id = 0 search from the begin
    * @param {Number} limit - The limit of one page
    * @param {Boolean} isVendor - Is vendor or not
    * @param {Dict} options - {from: msg.sender}
    * @returns {Promise} {roomnightIds: BigNumber|Array, nextId: BigNumber}
    */
  roomNightsOfOwner(from, limit, isVendor, options) {
    return new Promise((resolve, reject) => {
      this.contract.roomNightsOfOwner(from, limit, isVendor, {
        from: options.from
      }, (err, res) => {
        if(err) {
          reject(err);
        }
        else {
          resolve({
            roomnightIds : res[0],
            nextId: res[1]
          });
        }
      });
    });
  }
}
```

## 语法
*建议* 使用 `let` 声明变量。

示例：
```javascript
// good
let name = 'jay';

// bad
var name = 'jay';
```

*强制* 每个 `let` 或者 `var` 只能声明一个变量。

示例：
```javascript
// good
let name = 'jay';
let title = 'hello';

// bad
var name = 'jay', title = 'hello';
```

*强制* 变量必须`即用即声明`，避免在函数或其它形式的代码块起始位置统一声明所有变量。

示例：
```javascript
// good
let array = [];

for (let i = 0; i < 10; i++) {
  array.push(i);
}

// bad
let i;
let array = [];

for (i = 0; i < 10; i++) {
  array.push(i);
}
```

*强制* 使用类型严格的 `===`。仅当判断 `null` 或 `undefined` 时，允许使用 `==`。

示例：
```javascript
// good
if (index === 10) {
  // ...
}

// bad
if (index == 10) {
  // ...
}
```

*建议* 尽可能使用简洁的表达式。

*建议* 类型检测优先使用 `typeof`。对象类型检测使用 `instanceof`。`null` 或 `undefined` 的检测使用 `== null`。

*强制* 字符串使用单引号 `''`

示例：
```javascript
// good
let name = 'jay';

// bad
let name = "jay";
```

*建议* 使用对象字面量 `{}` 创建新 `Object`。

示例：
```javascript
// good
let obj = { };

// bad
let obj = new Object();
```

*建议* 属性访问时，尽量使用 `.`。

示例：
```javascript
// good
let name = obj.name;

// bad
let name = obj['name'];
```

*建议* 使用数组字面量 `[]` 创建新数组

示例：
```javascript
// good
let array = [];

// bad
let array = new Array();
```

*建议* 一个函数的参数控制在 `6` 个以内。

示例：
```javascript
// good
function fun (name, title) {
  // ...
}

// bad
function fun (name, title, c, d, e, f, g) {
  // ...
}
```

*建议* 通过 `options` 参数传递非数据输入型参数。

示例：
```javascript
// good
function fun (name, title, url) {
  // ...
}

// bad
function fun (name, options) {
  if (options.title) {
    // ...
  }

  if (options.url) {
    // ...
  }
}
```

*强制* 不允许使用直接 `eval` 函数。

示例：
```javascript
// bad
let str = 'console.log("hello world")';
eval(str);
```

*建议* 尽量不要使用 `with`。

*建议* 减少 `delete` 的使用。

示例：
```javascript
// bad
let obj = {
  name: '',
  title: ''
};
delete obj.name;
```

## 面向对象
TODO