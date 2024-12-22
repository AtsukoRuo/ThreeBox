# JS

JavaScript 的功能很大程度上取决于它运行的环境。例如，[Node.js](https://wikipedia.org/wiki/Node.js) 支持允许 JavaScript 读取/写入任意文件，执行网络请求等的函数。浏览器中的 JavaScript 仅支持有关网页的操作，而且大部分功能（访问文件）受到限制。





将 JavaScript 代码添加到页面中的两种方式（二选一）：

- 在  `<script>` 标签内编写代码：

  ~~~js
  <script>
    	alert(1);
  </script>
  ~~~

- 通过 `<script>`的 `src` 属性指定一个外部脚本

  ~~~js
  <script src="path/to/script.js"></script>`
  ~~~

  

ES5 规范新增了一些特性，并且修改了一些已存在的特性。考虑到兼容性，大部分的修改默认是不生效的。此时，必须使用 `"use strict"`指令来明确地激活这些特性。此外， use strict 将强制要求编写更加严格的代码。

~~~JavaScript
"use strict";

// 代码以现代模式工作
...
~~~

- 请确保 `"use strict"` 出现在脚本的最顶部
- 一旦进入了严格模式，就无法退出该模式
- 一旦使用了 class 以及 module 特性，那么 JS 引擎就自动以严格模式来执行代码





变量的声明：

~~~js
let user = 'John', age = 25, message = 'Hello';
~~~

变量命名有两个限制：

1. 变量名称必须仅包含字母、数字、符号 `$` 和 `_`。
2. 首字符必须非数字。
3. 区分大小写

在严格模式下，必须先定义再赋值：

~~~js
"use strict";
num = 5; // 错误：num 未定义
~~~

~~~js
// 注意：这个例子中没有 "use strict"
num = 5; // 如果变量 "num" 不存在，就会被创建
~~~



通过 const 来声明运行时常量：

~~~js
const COLOR_ORANGE = "#FF7F00";
~~~



JavaScript 是动态类型语言，即变量并不会在定义后，被限制为某一数据类型。

~~~JavaScript
// 没有错误
let message = "hello";
message = 123456;
~~~





- Number 类型：代表整数、浮点数、NaN、Infinity，支持乘法 `*`、除法 `/`、加法 `+`、减法 `-` 等等操作。

   ~~~JavaScript
   "not a number" / 2 === NaN		// NaN，这样的除法是错误的
   1 / 0 === Infinit
   ~~~

- BigInt：任意长度的整数

- string：字符串

- boolean

- null

- undefined

- symbol

- object