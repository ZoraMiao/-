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
## Js变量
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
## JS数据类型
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
### JavaScript 数组
* 有三种形式
```
    <script>
        //①
        //var arrays = new Array("cat","dog","pig");
        //②
        //var arrays = ["cat","dog","pig"];
        //③
        var arrays = new Array();
        arrays[0] = "cat";
        arrays[1] = "pig";
        arrays[2] = "dog";
        for(var i=0; i<arrays.length; i++){
            document.write(arrays[i] + "<br>");
        }
    </script>
```
### JavaScript 对象
* 对象由花括号分隔。在括号内部，对象的属性以名称和值对的形式 (name : value) 来定义。属性由逗号分隔：
```
    <script>
        var person = {name:"zhangmiao", age:20, school:"河工大"}
        document.write(person.name + "<br>");//第一种寻址方式
        document.write(person["age"] + "<br>");//第二种寻址方式
        document.write(person.school + "<br>");
    </script>
```
### Undefined 和 Null
* Undefined 这个值表示变量不含有值。
* 可以通过将变量的值设置为 null 来清空变量
```
		<script>
			var person;
			var car = "Volvo";
			document.write(person + "<br>");//undefined
			document.write(car + "<br>");//Volvo
			car = null;
			document.write(car + "<br>");//null
		</script>
```
### 声明变量类型
* 当您声明新变量时，可以使用关键词 "new" 来声明其类型：
```
var carname=new String;
var x=      new Number;
var y=      new Boolean;
var cars=   new Array;
var person= new Object;
```
* JavaScript 变量均为对象。当您声明一个变量时，就创建了一个新的对象
## Js对象
* **JavaScript 中的所有事物都是对象：字符串、数字、数组、日期、函数，等等。在 JavaScript 中，对象是拥有属性和方法的数据**
### 属性和方法
* 属性是与对象相关的值。
* 方法是能够在对象上执行的动作
### JavaScript 中的对象
* 在 JavaScript 中，对象是数据（变量），拥有属性和方法。
* 当这样声明一个 JavaScript 变量时：
  * var txt = "Hello";
* 实际上已经创建了一个 JavaScript 字符串对象。字符串对象拥有内建的属性 length。对于上面的字符串来说，length 的值是 5。字符串对象同时拥有若干个内建的方法。
* **在面向对象的语言中，属性和方法常被称为对象的成员。**
## Js函数
* **函数是由事件驱动的或者当它被调用时执行的可重复使用的代码块。**
### JavaScript 函数语法
* 函数就是包裹在花括号中的代码块，前面使用了关键词 function：
```
function functionname()
{
  这里是要执行的代码
}
```
* 当调用该函数时，会执行函数内的代码。
* 可以在某事件发生时直接调用函数（比如当用户点击按钮时），并且可由 JavaScript 在任何位置进行调用。
* **提示：JavaScript 对大小写敏感。关键词 function 必须是小写的，并且必须以与函数名称相同的大小写来调用函数。
### 调用带参数的函数
* 在调用函数时，可以向其传递值，这些值被称为参数。
* 这些参数可以在函数中使用。
* 可以发送任意多的参数，由逗号 (,) 分隔：
  * myFunction(argument1,argument2)
* 当声明函数时，请把参数作为变量来声明：
```
function myFunction(var1,var2)
{
  这里是要执行的代码
}
```
* 变量和参数必须以一致的顺序出现。第一个变量就是第一个被传递的参数的给定的值，以此类推
### JavaScript 变量的生存期
* JavaScript 变量的生命期从它们被声明的时间开始。
* 局部变量会在函数运行以后被删除。
* 全局变量会在页面关闭后被删除。
### 向未声明的 JavaScript 变量来分配值
* 如果把值赋给尚未声明的变量，该变量将被自动作为全局变量声明。
* 这条语句：
  * carname="Volvo";
* 将声明一个全局变量 carname，即使它在函数内执行。
### JS运算符
* **如果把数字与字符串相加，结果将成为字符串。**
## JS比较与逻辑运算符
* `===`运算符，比较的是`值和类型`，例如x = 5,x === "5" 为false，因为类型不相同。
## JS条件语句
* if or if...else  or if...else if...else
* switch
### switch
* switch 语句用于基于不同的条件来执行不同的动作。
* default 关键词
  * 用 default 关键词来规定匹配不存在时做的事情
## JS 循环
* 循环可以将代码块执行指定的次数。
* 不同类型的循环
  * JavaScript 支持不同类型的循环：
  * for - 循环代码块一定的次数
  * for/in - 循环遍历对象的属性
  * while - 当指定的条件为 true 时循环指定的代码块
  * do/while - 同样当指定的条件为 true 时循环指定的代码块
### for循环
```
for (语句 1; 语句 2; 语句 3)
  {
  被执行的代码块
  }
```
* **语句 1
  * 通常我们会使用语句 1 初始化循环中所用的变量 (var i=0)。
  * 语句 1 是可选的，也就是说不使用语句 1 也可以。
  * 可以在语句 1 中初始化任意（或者多个）值：
```
for (var i=0,len=cars.length; i<len; i++)
{
  document.write(cars[i] + "<br>");
}
```
* **语句 2
  * 通常语句 2 用于评估初始变量的条件。
  * 语句 2 同样是可选的。
  * 如果语句 2 返回 true，则循环再次开始，如果返回 false，则循环将结束。
  * 提示：如果省略了语句 2，那么必须在循环内提供 break。否则循环就无法停下来。这样有可能令浏览器崩溃。
* **语句 3
  * 通常语句 3 会增加初始变量的值。
  * 语句 3 也是可选的。
  * 语句 3 有多种用法。增量可以是负数 (i--)，或者更大 (i=i+15)。
  * 语句 3 也可以省略（比如当循环内部有相应的代码时）
```
var i=0,len=cars.length;
for (; i<len; )
{
  document.write(cars[i] + "<br>");
i++;
}
```
### For/In 循环
* JavaScript for/in 语句循环遍历对象的属性
```
var person={fname:"John",lname:"Doe",age:25};
for (x in person)
{
  txt=txt + person[x];
}
```
### while循环
### do/while 循环
* do/while 循环是 while 循环的变体。该循环会执行一次代码块，在检查条件是否为真之前，然后如果条件为真的话，就会重复这个循环。
```
do
  {
  需要执行的代码
  }
while (条件);
```
### Break 和 Continue 语句
* break 语句用于跳出循环。
* continue 用于跳过循环中的一个迭代。
* **JavaScript 标签
  * 如需标记 JavaScript 语句，请在语句之前加上冒号： label：语句
  * break 和 continue 语句仅仅是能够跳出代码块的语句
  * continue 语句（带有或不带标签引用）只能用在循环中。
  * break 语句（不带标签引用），只能用在循环或 switch 中。
  * 通过标签引用，break 语句可用于跳出任何 JavaScript 代码块：
```
cars=["BMW","Volvo","Saab","Ford"];
list:
{
	document.write(cars[0] + "<br>");
	document.write(cars[1] + "<br>");
	document.write(cars[2] + "<br>");
	break list;
	document.write(cars[3] + "<br>");
	document.write(cars[4] + "<br>");
	document.write(cars[5] + "<br>");
}
```
## JavaScript 错误 - Throw、Try 和 Catch
* try 语句测试代码块的错误。
* catch 语句处理错误。
* throw 语句创建自定义错误。
```
try
  {
  //在这里运行代码
  }
catch(err)
  {
  //在这里处理错误
  }
```
### Throw 语句
* throw 语句允许我们创建自定义错误。
* 正确的技术术语是：创建或抛出异常（exception）。
* 如果把 throw 与 try 和 catch 一起使用，那么您能够控制程序流，并生成自定义的错误消息。
* 语法: throw exception
* 异常可以是 JavaScript 字符串、数字、逻辑值或对象
# JS DOM(文档对象模型)
* **查找 HTML 元素
  * 通过 id 找到 HTML 元素  //getElementById
  * 通过标签名找到 HTML 元素//getElementsByTagName
  * 通过类名找到 HTML 元素
## DOM HTML
* **HTML DOM 允许 JavaScript 改变 HTML 元素的内容。
### 改变 HTML 输出流
* 在 JavaScript 中，document.write() 可用于直接向 HTML 输出流写内容。
* 提示：**绝不要使用在文档加载之后使用 document.write()。这会覆盖该文档。
### 改变 HTML 内容
* 修改 HTML 内容的最简单的方法时使用 innerHTML 属性。
* 如需改变 HTML 元素的HTML DOM 允许 JavaScript 改变 HTML 元素的样式内容，请使用这个语法：
  * document.getElementById(id).innerHTML=new HTML
### 改变 HTML 属性
* 如需改变 HTML 元素的属性，请使用这个语法：document.getElementById(id).attribute=new value
## DOM CSS
* **HTML DOM 允许 JavaScript 改变 HTML 元素的样式
### 改变 HTML 样式
* 如需改变 HTML 元素的样式，请使用这个语法：document.getElementById(id).style.property=new style
* 隐藏文本：document.getElementById('demo').style.visibility = 'hidden'
* 显示文本：document.getElementById('demo').style.visibility = 'visible'





















