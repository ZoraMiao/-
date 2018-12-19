### HTML 中的脚本必须位于 <script> 与 </script> 标签之间。
### 脚本可被放置在 HTML 页面的 <body> 和 <head> 部分中。
* 通常的做法是把函数放入 <head> 部分中，或者放在页面底部。这样就可以把它们安置到同一处位置，不会干扰页面的内容。
  
### 外部的JavaScript
* 也可以把脚本保存到外部文件中。外部文件通常包含被多个网页使用的代码。
* 外部 JavaScript 文件的文件扩展名是 .js。
* 如需使用外部文件，请在 <script> 标签的 "src" 属性中设置该 .js 文件
* **外部脚本不能包含 <script> 标签。**
  
### 操作 HTML 元素
* 如需从 JavaScript 访问某个 HTML 元素，您可以使用 document.getElementById(id) 方法。
* 请使用 "id" 属性来标识 HTML 元素
* `document.getElementById("demo").innerHTML="我的第一段 JavaScript";`浏览器将访问 id="demo" 的 HTML 元素，并把它的内容（innerHTML）替换为 "My First JavaScript"。
* 使用 document.write() 仅仅向文档输出写内容。如果在文档已完成加载后执行 document.write，整个 HTML 页面将被覆盖
### 分号";"
* 分号用于分隔 JavaScript 语句。
* 通常我们在每条可执行的语句结尾添加分号。
* 使用分号的另一用处是在一行中编写多条语句。
* **在 JavaScript 中，用分号来结束语句是可选的。**
### JavaScript 代码
* JavaScript 代码（或者只有 JavaScript）是 JavaScript 语句的序列。
* 浏览器会按照编写顺序来执行每条语句。
### JavaScript 代码块
* JavaScript 语句通过代码块的形式进行组合。
* 块由左花括号开始，由右花括号结束。
* 块的作用是使语句序列一起执行。
* JavaScript 函数是将语句组合在块中的典型例子。
### JavaScript 对大小写敏感。
* JavaScript 对大小写是敏感的。
* 当编写 JavaScript 语句时，请留意是否关闭大小写切换键。
* 函数 getElementById 与 getElementbyID 是不同的。
* 同样，变量 myVariable 与 MyVariable 也是不同的。
### 变量是存储信息的容器
* 变量必须以字母开头
* 变量也能以 $ 和 _ 符号开头（不过我们不推荐这么做）
* 变量名称对大小写敏感（y 和 Y 是不同的变量）
### 声明（创建） JavaScript 变量
* 在 JavaScript 中创建变量通常称为“声明”变量。
* 使用 var 关键词来声明变量：
```
var carname;
```
* 变量声明之后，该变量是空的（它没有值）。
* 如需向变量赋值，请使用等号：
```
carname="Volvo";
```
* 不过，也可以在声明变量时对其赋值：
```
var carname="Volvo";
```
### Value = undefined
* 在计算机程序中，经常会声明无值的变量。未使用值来声明的变量，其值实际上是 undefined。
* 在执行过以下语句后，变量 carname 的值将是 undefined：
```
var carname;
```
### 重新声明 JavaScript 变量
* 如果重新声明 JavaScript 变量，该变量的值不会丢失：
* 在以下两条语句执行后，变量 carname 的值依然是 "Volvo"：
```
var carname="Volvo";
var carname;
```
### JavaScript 拥有动态类型
* JavaScript 拥有动态类型。这意味着相同的变量可用作不同的类型：
```
var x                // x 为 undefined
var x = 6;           // x 为数字
var x = "Bill";      // x 为字符串
```
### JavaScript 字符串
* 字符串是存储字符（比如 "Bill Gates"）的变量。
* 字符串可以是引号中的任意文本。您可以使用单引号或双引号
* 可以在字符串中使用引号，只要不匹配包围字符串的引号即可
```
var answer="Nice to meet you!";
var answer="He is called 'Bill'";
var answer='He is called "Bill"';
```
### JavaScript 数字
* JavaScript 只有一种数字类型。数字可以带小数点，也可以不带
* 极大或极小的数字可以通过科学（指数）计数法来书写
```
var x1=34.00;      //使用小数点来写
var x2=34;         //不使用小数点来写
var y=123e5;      // 12300000
var z=123e-5;     // 0.00123
```
### JavaScript 布尔
* 布尔（逻辑）只能有两个值：true 或 false






