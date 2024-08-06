# Java Script

**组件库&框架:**

  H-ui（admin组件库）、Element-ui（pc端组件库）、Vant（移动端组件库）、Vue3（前端框架）、jQuery、



**JavaScript是一种脚本语言，可以提高用户提高用户体验度。（依托于浏览器）引擎是浏览器Javascript是跨平台的，为什么跨平台？以为依托于浏览器，不依托于操作系统**

##### JavaScript更像是一门函数式编程语言。

```html

<script type="text/javascript"></script>
<!-- 可以放在body里面也可以放在外边，也可以放在head里面 -->
        
```

#### JavaScript 组成部分：

ECMAScript 核心 

DOM 文档对象模型 

BOM 浏览器对象模型 

##### 三目运算符也叫三元运算符： 

 例如： 
```js

// 如果条件成立就会把第一个值赋给 c 这就是三目运算符
let c = a > b ? a : b;

// 合并空值运算符
let a = undefined;
let b = 'hello world'
let c = a ?? b;  // 过滤 undefined 和 null 返回 b 的值；

```
#### JavaScript引入方式：内部引用；外部引用；
```html

<!-- 内部引用：-->
<script  type="text/javaScript">
	//在这里写JS代码...
</script>
<!-- 内部JavaScript，指的是把HTML代码和JavaScript代码放在同一个文件中。 -->


<!-- 外部引用：-->
<script src="/index.js"></script>
<!-- 可以在head中引用 也可以在body中引用 -->

```


######  

**在JavaScript中，每一条语句都是英文分号 ';' 作为结束符。每一条语句都有它特定的功能。如果只写了 ';'号那就是空语句的意思**

```js

var a = 10；   //直接赋值    var声明符   a变量名    = 赋值符  10值     ；语句块结束符号

// alert  警告；告诫 在JavaScript中意思为弹出框警告的意思     else否则     int整数   parse强制       parseint强制整数
 alert();  //在网页弹出一个对话框      

//   \n 在浏览器中换行
//   \r在IE浏览器中换行。


document.write("");基本网页显示的一种语法语法
var a = 1; //初始化赋值
a = Number(prompt("请输入一个值"); //弹窗语法
// 变量 <= 赋值
           
```



#### 变量名 命名规则：
在JavaScript中，变量指的是一个可以改变的量。也就是说，变量的值在程序运行过程中是可以改变的
变量由字母、下划线、$或数字组成，并且第一个字母必须是“字母、下划线或$”；

变量不能是系统关键字和保留字

**注意：JavaScript的变量名区分大小写，A 和 a 是两个不同的变量。**



#### 数据类型：

**引用数据类型：** Object {}(对象)   Array [](数组)

**数字类型**： 10(整数)  -10(负数)  1.1(浮点类型)  Number(数字类型)

**字符串类型：** "hello world" String(字符串类型)

**布尔值类型：** false、true  boolean(布尔值)

**特殊数据类型：** null、undefined



#### JavaScript标识符（命名规则）
标识符由字母、数字、下划线_、美元符号$、组成

不能以数字开头、不能是系统关键字、严格区分字母大小写、不能以中划线开头、不能包含中划线

标识符（identifier）指的是用来识别各种值的合法名称。最常见的标识符就是变量名。

= 一个等于是赋值
== 两个等于是判值判断关系运算赋是否相等
=== 三个等于是判断类型（全等于）



**关系运算符：** 小于 <    大于 >    小于等于 <=     大于等于 >=    不等于 !=

**逻辑运算符：**逻辑&&两者都为真，则为真。逻辑 | | 其中一个为真，则为真。

**逻辑！:**    取相反值，本来是真 加入！之后就变成假了

**算数运算符：**等于 ==     左加 +=      左减 -=       左乘 *=       左除 /=       左

取余 %=

++i;    i++; 自增   自减     特殊记

++i：指的是先运算，再赋值。

i++：指的是先赋值，再运算


#### 运算符优先级关系：
逻辑非！非 > 算数 > 关系 > 逻辑&&逻辑|| > 赋值   （有括号的的先算括号的）

最基本数据类型5种：数字、字符串、布尔值、未定义置和空值

引用数据类型2种：数组、对象

一切非零的正整数都为真true     零代表假false

```js

//先判断条件，在执行循环
var  i=1；初始值：只执行一次
while (循环条件：判断布尔值) {
	循环体
  	i++；（计步器，是循环趋近于结束）
} 
// ; 代表空语句

//先执行，在判断条件
do {
	//要执行的代码段
} while (循环条件)

```

isNaN()判定字母如果是字母返回true，如果不是返回false

###### 短路效应

逻辑&&第一个表达式不成立第二个表达式不运行

逻辑 | | 第一个表达式成立第二个表达式不运行

###### 五大核心浏览器：火狐Firefox   谷歌Google    IE浏览器（InternetExplorer）   苹果浏览器Safai    欧鹏浏览器

##### 分支结构

单分支，双分支，多分支

```js

// 单分支  
if(条件) { 
	// 执行代码..
}

// 双分支  
if(条件) {
    // 条件成立执行代码..
} else {
    // 条件不成立执行代码..
}

// 多分支  
if(条件) {
	// 条件成立执行代码..
} else if(条件) {
	// 第二个条件成立执行代码..
    // 可以写无数个 else if..
} else {
    // 条件不成立执行代码..
}

```

#### **switch：**

​	一种比 if 读取快，写起来比 if 多；**switch** 只能判断一个值，不能判断范围，而 if 可以判断范围。

```js

// 例如：
var num = 1；
switch (num) {
 case 1:
 // num的值等于1时触发的代码段 ;
 break; // 注意：没有break；的时候从没有break；往下的都会输出一遍

 case n:
 // 以此类推 等于n时.. ;
 break;

 default:
 // 以上条件都不符合时，默认执行的代码段；
 break;
}


break; // 结束全部循环
continue; //结束本次循环，结束一次循环（直接跳到循环条件的地方）

 //for 循环的执行顺序 1‐2‐3‐5‐6‐7‐9‐8‐7‐9‐8‐7‐4‐10‐11
 for( 2 ; 3 ; 4 ){  // 再来到这个循环里，重新循环
     for( 6 ; 7 ; 8 ){
      9  // 如果这里有break; 那他就直接结束只一个循环
     }
    10
 }
 11

 do {
 // 循环体
 } while (循环条件)
// 先执行，再判断条件 while先判断条件再执行代码 其实while和do while是一样的
     
// 函数
function 函数名(形参) {
	 //执行体
 	}
}

// 使用函数
函数名(实参);

// JS 取余
if(a % 2 == 0 ) {
 //取余
}

```
##### window.onload   告诉计算机等到页面加载完了以后在执行的代码

计时器或者叫定时器：

 setTimeout（"需执行的函数",1000毫秒）；意思过多少秒执行一次的

 setInterval   ("需要执行的函数"，时间毫秒)；意思每过多少时间执行一次的代码；

手动结束的话用  clearTimeout(id)清除timeout的     clearInterval(id)清除interval的

### 数组：

```js

// 索引值是从0开始
var arr = [ x ] [ y ];
var arr [ x ] = 1;

// 声明一个数组
var arr = new Arry([2,3,4]);

```

#### 数组遍历：

```js

let array = [1, 2, 3, 4, 5, 6, 7, 8,, 10, 11];
for(let i = 0;i < array.length; i++) {
    if(array[i] == 5) {
        break; // 1 2 3 4 
        continue; // 1 2 3 4 6 7 8 undefined 10 11
    }
}

for(item of array) {
    if(item == 5) {
        break; // 1 2 3 4 
        continue; // 1 2 3 4 6 7 8 undefined 10 11
    }
}

array.forEach((item,index,arr) => {
    if(item == 5) {
        console.log(index) // 0 1 2 3 4 5 6 7 8 9 10
        console.log(item) // 1 2 3 4 6 7 8  10 11
    }
})

```
**以上三种遍历方式总结：**
	三者都是基本的从左到右遍历数组
	forEach 无法跳出循环；for、for...of 可以使用 break；continue；跳出循环或中断。
	for...of 直接访问的是实际元素。for 遍历数组索引，forEach 回调函数更丰富，元素、索引、原数组都可以获取。
	for、for...of 数组中有空元素同样会执行。









```js

let array = [
    {
        name: '头部导航',
        backward: false
    },
    {
        name: '轮播',
        backward: true
    },
    {
        name: '页脚',
        backward: false
    },
]
someBackward = array.some(item => item.backward);
// someBackward true;
everyBackward = array.every(item => item.backward);
// everyBackward false;

```

**以上两种遍历方式总结：**
	二者都是采用数组条件判断的，都会返回一个布尔值
	二者都可以被中断
	some 其中某一个元素满足条件时，返回 true 遍历中断；所有元素不满足条件时，返回 false。
	every 其中某一元素不满足条件时，返回 false 遍历中断；所有元素都满足条件时，返回 true。









```js

let array = [
    { 
        name: '头部导航', 
        type: 'nav',
        id: 1
    },
    {
        name: '轮播', 
        type: 'content',
        id: 2 
    },
    {
        name: '页脚', 
        type: 'nav',
        id: 3 
    },
]
let newArray = array.filter(item => {
    console.log(item);
    return item.type == 'nav';
});
/* newArray 
	[
		{ name: '头部导航', type: 'nav', id: 1 },
		{ name: '页脚', type: 'nav', id: 3 },
	]
*/

let newArray = array.map(item => {
    console.log(item);
    return item.id;
})
/* newArray
	[ 1, empty, 2, 3 ]
*/

```

**以上两种遍历方式总结：**
	二者都会生成一个新数组，不会改变原数组（不包括遍历对象数组，在回调函数中操作元素对象）
	二者都会跳过空元素。
	map 会将回调函数返回成一个新数组，数组长度与原数组一致。
	filter 会将符合函数条件的元素组成一个新数组，数组长度于原数组不一致。
	map 生成的新数组元素是可自定义。
	filter 生成的新数组元素不可自定义，与对应原数组元素一致。










```js

let array = [
    {
        name: '头部导航',
        id: 1
    },
    {
        name: '轮播',
        id: 2
    },
    {
        name: '页脚',
        id: 3
    },
]
let reslut = array.find(item => item.id == 1);
/*
	result {
		name: '头部导航',
		id: 1
	}
*/
result.name = '头部'
/*
 array [
 	{ name: '头部', id: 1 },
 	{ name: '轮播', id: 2 },
 	{ name: '页脚', id: 3 },
 ]
*/

let index = array.findIndex(item => return item == 2)
// index  1

```

**以上两种方式总结：**
	二者都是用来查找数组元素。
	find 返回数组中满足回调函数的条件的第一个元素的值。如果不存在返回 undefined
	findIndex 返回数组中满足回调函数的索引，如果没有返回 -1









```js

let array = [
    {
        name: 'left',
        width: 20
    },
    {
        name: 'center',
        width: 70 
    },
    {
        name: 'right',
        width: 10 
    },
]
let total = array.reduce((currentTotal,item) => {
    return currentTotal + item.width;
})
// total: 100

```

**reduce 总结：**

​	reduce 接收两个参数 callback 和 initValue 回调函数和初始值

​	reduceRight 和 reduce 一样，只不过 reduceRight 是从右边开始的

​	计算数组元素相加的总和











#### Base 64：

JavaScript 内置函数，用来转换成 Base64 编码，**Nodejs 中没有改名命令**

```js

// base64 解密
atob(base65值)

// base64 加密
btoa(要加密的值)

```







##### eval（" num = 7 "）把里面的字符串当代码执行

被除数      除数      商

10    ÷     5    =   2   

**console.log ( )  把括号里面的东西打印在控制台**

**console.error() 抛出异常**

**console.trace() 方法用于显示当前执行的代码在堆栈中的调用路径。**

**console.info() **

**console.dir()**

可以调样式：console.log('%c params ', 'color: white; background-color: #f00000', params);





求余 10 % 4 = 2 ； 这就是求余   2 * 4 = 8    10 - 8 = 2 所以余数是二



Unicode 统一的字符编码标准

ASCII码 鼠标和键盘编码

##### JS ASII码 键盘事件绑定：

```js

document.onkeydown(e) {
    let e = e ? e : event; //如果 e 不能用 就把 event 赋值给 e
    if(e.keyCode ==  32 ){
     //空格事件
    }
}

//给 id 为 input 添加事件
var input = document.getElementById("input");
input.onkeypress = function (e){
		if(e.key == "Enter"){
            console.log("触发Enter事件了")
        }
}

```

[查询ASCII码](http://ascii.911cha.com/)



**键盘事件：**

| 属性       | 说明                                                         |
| ---------- | ------------------------------------------------------------ |
| keyCode    | 该属性包含键盘中对应键位的键值                               |
| charCode   | 该属性包含键盘中对应键位的 Unicode 编码，仅 DOM 支持         |
| target     | 发生事件的节点（包含元素），仅 DOM 支持                      |
| srcElement | 发生事件的元素，仅 IE 支持                                   |
| shiftKey   | 是否按下 Shift 键，如果按下返回 true，否则为false            |
| ctrlKey    | 是否按下 Ctrl 键，如果按下返回 true，否则为false             |
| altKey     | 是否按下 Alt 键，如果按下返回 true，否则为false              |
| metaKey    | 是否按下 Mtea 键，如果按下返回 true，否则为false，仅 DOM 支持 |

| 键位                    | 码值  | 键位                   | 码值  |
| ----------------------- | ----- | ---------------------- | ----- |
| 0~9（数字键）           | 48~57 | A~Z（字母键）          | 65~90 |
| Backspace（退格键）     | 8     | Tab（制表键）          | 9     |
| Enter（回车键）         | 13    | Space（空格键）        | 32    |
| Left arrow（左箭头键）  | 37    | Top arrow（上箭头键）  | 38    |
| Right arrow（右箭头键） | 39    | Down arrow（下箭头键） | 40    |

| 属性                 | IE 事件模型                                                  | DOM 事件模型                                                 |
| -------------------- | ------------------------------------------------------------ | ------------------------------------------------------------ |
| keyCode（keypress）  | 返回所有字符键的正确值，区分大写状态（65~90）和小写状态（97~122） | 功能键返回正确值，而 Shift、Ctrl、Alt、PrintScreen、ScrollLock 无返回值，其他所有键值都返回 0 |
| keyCode（keydown）   | 返回所有键值（除 PrintScreen 键），字母键都以大写状态显示键值（65~90） | 返回所有键值（除 PrintScreen 键），字母键都以大写状态显示键值（65~90） |
| keyCode（keyup）     | 返回所有键值（除 PrintScreen 键），字母键都以大写状态显示键值（65~90） | 返回所有键值（除 PrintScreen 键），字母键都以大写状态显示键值（65~90） |
| charCode（keypress） | 不支持该属性                                                 | 返回字符键，区分大写状态（65~90）和小写状态（97~122），Shift、Ctrl、Alt、PrintScreen、ScrollLock 无返回值，其他所有键值都返回 0 |
| charCode（keydown）  | 不支持该属性                                                 | 所有键值为 0                                                 |
| charCode（keyup）    | 不支持该属性                                                 | 所有键值为 0                                                 |





mouseover 事件在鼠标移动到选取的元素及其子元素上时触发 。

mouseenter 事件只在鼠标移动到选取的元素上时触发。

#### 冒泡排序法：

##### 思路：

(1)比较两个相邻的元素，如果后一个比前一个大，则交换位置

(2)第一轮的时候最后一个元素应该是最大的一个

(3)按照第一步的方法进行两个相邻的元素的比较，由于最后一个元素已

##### 经是最大的了，所以最后一个元素不用比较。

```js

var list = [ 45, 4, 6, 1, 14, 55, 10, 9 ];
function sort(list) {
 for (i = 0; i < list.length; i++) {
     for (j = 0; j < list.length - 1 ‐ i; j++) {
         if (list[j] < list[j+1]) {
             b = list[j];
             list[j] = list[j+1];
             list[j+1] = b;
         }
     }
 }
 for(k in list) {
     document.write(list[k]+"<br/>");
 }
}
// 执行函数
sort(list);

```
#### 递归：

1.假设递归函数已经写好

2.寻找递推关系

3.将递推关系的结构转换为递归体

4.将临界条件加入到递归体中

```js

//简单的递归
function sum () {
    if (n == 1) {
        return ;
    }
    return sum(n * 1) + n
}

// 一个简单的阶乘函数
var fn = function(x) {
    if (x ===  1) {
     	return  1;
     } else {
    	return x * fn(x ‐ 1);
	 }
 }

// 递归方法 ：
function fib(n) {
	 if (n ===  1  || n ===  2) {
         return n ‐  1;
     }  
    return fib(n ‐ 1) + fib(n ‐ 2);
 }
console.log(fib( 10 )) 

 //非递归方法 
 function fib(n) {
     let a =  n;
     let b =  a + n;
     let c = a + b;
     for (let i =  3; i < n; i++) {
         a = b 
         b = c
         c = a + b
     }
	 return c
 }
  console.log(fib( 10 )) 

```
###### JS 日期函数:

```js

var date = new Date();      //创建一个新的日期对
 Timestamp = date.getTime()  //获取时间戳
 Years = date.getFullYear()  //获取四位数 年份
 Month = date.getMonth()     //以(0~11) 获取月份
 d = date.getDate()          //获取日期 日
 Hours = date.getHours()     //以(0~23) 获取小时数
 Minutes = date.getMinutes() //获取方法 描述

getDate() 			// 以数值返回天（1-31）
getDay() 			// 以数值获取周名（0-6）
getFullYear() 		// 获取四位的年（yyyy）
getHours() 			// 获取小时（0-23）
getMilliseconds() 	// 获取毫秒（0-999）
getMinutes()		// 获取分（0-59）
getMonth()			// 获取月（0-11）
getSeconds()		// 获取秒（0-59）
getTime()			// 获取时间（从 1970 年 1 月 1 日至今）

```

### JavaScript Class 类：

Class 是 ES6 中引入的一种面向对象语法糖。它不是一种新的面向对象继承模型，而是基于原型的继承模型的语法糖。

ES6 之前，我们使用构造函数和原型来定义对象和实现继承；

```js

// ES6之前写法
function Person (name) {
    this.name = name;
}
Person.prototype.sayName = function () {
    console.log(this.name)
}

// Class写法
class Person {
    // 私有变量方法属性前面用 # 号。私有成员只能在类内部访问。
    // #sex;
    
    // 静态方法：static 关键字来定义。静态方法属于类本身，而不是实例。
    static sayValue () {
        return 'Hello World';
    }
    // 静态方法是可以直接访问静态方法的，但不能访问实例方法属性
    static say () {
        alert(this.sayValue());
    }
    constructor (name,sex) {
        this.name = name;
        this.#sex = sex;
    }
    sayName() {
        console.log(this.name);
    }
	// getter 和 setter 用来设置直接访问的属性值或直接修改属性值的方法。
	set address(value) {
        this.address = value;
    }
	get address(value) {
        return '地址：' + this.address;
    }
}
// 实例化Class 
const person = new Person('王康', '男');
person.sayName();
person.address = '中国山东省临沂市';
console.log(person.address); // 地址：中国山东省临沂市
person.say();   // HelloWorld
// 可以看到 Class 更加清晰，易于理解

// Class 继承
class Student extends Person {
    constructor (name,number) {
        // 使用 super 调用父类构造函数
        super(name);
        this.number = number;
    }
}

```



## Node.js:

简单的说 Node.js 就是运行在服务端的 JavaScript。

Node.js 是一个基于Chrome JavaScript 运行时建立的一个平台。

Node.js是一个事件驱动I/O服务端JavaScript环境，基于Google的V8引擎，V8引擎执行Javascript的速度非常快，性能非常好。

### Node.js 安装包及源码下载地址为：https://nodejs.org/en/download/。

简单示例：

```js

// 创建一个应用
 const http = require("http");  // http 网络请求模块
 const fs = require("fs"); 		// fs 系统操作模块
 const url = require("url");	// url url地址截取模块

// 创建一个HTTP服务
 http.createServe(function (request, response) {
     /* 
     设置响应头  设置内容编码格式
     第一个参数是( 200 ,{"Content‐type" 设置状态码 :"text‐plain;charset=utf8;"}) 也 转换
     */
	 response.setHeader("Content‐type","text/html;charset=utf8;"); 
     response.wirteHead
     
     // 把 url GET 传的值格式 加文件名
     let query  urlData 是接收= urlGET值.parse true (是执行request.url,true).query; 
     //读取文件 参数是文件名 或 路径 参数是值，如果没有该文件会创建该文件，如果有内容则会覆盖。
     let txtData 
     // 加上Sync=意思是执行同步 
     fs.readFileSync('test.txt');
     //写入文件 第一个参数和读取文件一样 第二个
     fs.wirteFile("test.txt",value); 
     //相应内容
	 response.end('hello world') 
     
 }).listent( 8888 ) //设置端口号

```




### Node Koa2框架： 封装原生代码的 API

```sh

# Node 安装Koa2 安装完成 不会自带 node_module 需要手动安装一下
npm i
# 安装koa2
npm i ‐g koa‐generator      	# 安装 koa-generator 脚手架 中间件

# 查看 版本
koa2 ‐‐version

# 创建项目
koa2 项目名称 		# 使用 koa-generator 脚手架 创建项目

# 运行项目
koa2 run dev 项目名称

```

#### Nodemon 插件：

介绍：nodemon是一种工具，可以自动检测到目录中的文件，更改时通过重新启动应用程序来调试基于node.js的应用程序。

```sh

#安装 nodemon
npm i ‐g nodemon                   #使用 npm 安装 ‐g 全局的 nodemon

#使用
nodemon 文件名或路径名加文件名       # 使用 nodemon 打开 node 服务

#nodemon 命令
rs 重启一下 是 restart 的缩写

```
### Node JWT Token：

**JWT**：

​	JSON Web Token是JSON对象的一种编码方式。它通过JSON对象来传递采用的信息，并且该信息是以数字签名的。由于数字签名，所以JWT也被称为JSON Web签名(JWS)。

​	JWT常用于身份验证，因为他以JSON格式存储用户信息，且该信息是可以通过签名。这使JWT很适用于身份验证。

​	JWT的组成部分：**header.payload.signature**

​		**header：**中包含含有关令牌类型和使用的算法信息。

​		**payload：**中包含声明或其它有用负载信息。

​		**signture：**是可选项，用来对前两部分的签名，防止篡改

```js

// 安装 jwt jsonwebtoken
npm install jsonwebtoken

//引用 jsonwebtoken
const jwt = require('jsonwebtoken');

// 登录成功 生成token
const token = jwt.sign({
	time: Date now(),
	timeout: Date now() +  60000,
	// 用户信息... 等等
},'token'),

// 解析验证token
let token = ctx.request.headers['token'];
const token = jwt.verify(token,'token');

```
### Node Mysql 连接数据库：

Nodejs环境下的MySQL数据库驱动程序。它允许Nodejs应用程序连接到MySQL数据库并执行查询；增删改查。

```js

//先安装 MySQL
npm install mysql

//使用
const mysql = require('mysql');

//配置 MySQL 文件 新建js文件 命名为db_config.js
const config = {
     host     : 'localhost',
     user     : 'root',
     password : 'root',
     port: '3306',
     database: 'koa2'
 }
module.exports = config ; //导出

//封装 新建js文件 命名为db.js
const mysql  = require('mysql');
const config = require('./db_config');
//创建连接池
let connection = mysql.createConnection(config);
connection.connect(); //开启连接
var query = (Sql) => {
return new Promise((resolve,reject) => {
        connection.query(Sql,function (err, result) {
            if(err) {
                 console.log('[UPDATE ERROR] ‐ ',err.message);
                 return ;
            }
            resolve(result); //执行完成 返回数据
		});
	})
}
// connection.end();  //关闭连接
module.exports = query; //导出

//使用
const query = require("../db.js")//引入
let data = await query(SQL语句)

```
### Node js  WebScoket：

WebSocket 使客户端和服务器端之间的数据交换变得更加简单，允许服务器主动向客户端推送数据。在 WebSocket API 中，浏览器和服务器只需要完成一次握手，两者之间就可以持久性的连接，并进行双向数据传输。

```js

// 安装 WebScoket
npm install ws

// 客户端使用
// 引入使用
const WebSocket = require("ws");
var ws = new WebSocket("ws:localhost:888");
// 打开连接
ws.onopen = function(e) {
	console.log("客户端：与服务器的连接已打开");
};
// 接收服务器端发的消息
ws.onmessage = function(e) {
	console.log(e.data)
	//document.getElementById("list").innerHTML += "<li>"+e.data+"</li>"
}
// 触发事件 发送消息
function sendMessage() {
	var message = document.getElementById("message").value;
	// console.log(message);
	ws.send(message);
};


// 服务器端使用如下
// 创建websocket服务
var WebSocketServer = require("ws").Server;

//设置端口号
wss = new WebSocketServer({port:888});

//查看 所有客户端
console.log(wss.clients)

//连接客户端
wss.on("connection",function (ws) {
	console.log("服务器端：客户端已连接");
	//接收客户端的消息
	ws.on("message",function(message) {
		console.log(message.toString())
		//发送消息到客户端
		ws.send(message.toString())
	})
})

```
**WebSocket事件：**

| 事件    | 事件处理程序     | 描述                       |
| :------ | :--------------- | :------------------------- |
| open    | Socket.onopen    | 连接建立时触发             |
| message | Socket.onmessage | 客户端接收服务端数据时触发 |
| error   | Socket.onerror   | 通信发生错误时触发         |
| close   | Socket.onclose   | 连接关闭时触发             |

**WebSocket方法：**

| 方法           | 描述             |
| :------------- | :--------------- |
| Socket.send()  | 使用连接发送数据 |
| Socket.close() | 关闭连接         |





#### Nodejs  Joi：

JavaScript对象的规则描述语言和验证器。

```js

const Joi = require('joi'); 	// joi 一个校验模块
Joi.string() / Joi.number() 	// 定义只能是字符串类型/数字类型
Joi.alphanum() 					// 只能是字母字符串或数字字符串
Joi.max() / Joi.min() 			// 限制最大字符串长度/限制最小字符串长度
Joi.required() 					// 此属性必填
Joi.error() 					// 定义错误信息
Joi.regex() 					// 接受一个字符串规则验证
Joi.integer() 					// 必须是整数

//对象验证
Joi.validate({ username: 'abc', birthyear:  1994  }, schema);

```


#### Node pm2：

是一个守护进程管理器，不会占用一个终端，而是在后台运行 js。



```shell

#安装
npm install pm2 -g

#运行 nodejs
pm2 start server.js

#监控
pm2 monit

#列出所有进程
pm2 list

#在koa2中运行
pm2 start bin/wwww --name="www"

#pm2自动启动 koa2
pm2 start bin/www --watch 

#停止所有进程
pm2 stop all

#重启所有进程
pm2 restart all

#关闭并删除所有应用
pm2 delete all

#删除指定应用
pm2 delete id

```



### Volta

Volta 是一种管理 JavaScript 命令行工具的便捷方式。

Volta 的优点就是：速度、无缝，每个项目的版本切换、跨平台支持、支持多个包管理器、稳定的工具安装、可拓展性。

```sh

# 查看各个工具的默认版本   显示当前工具链
volta list 

# 安装某个工具的版本 or 也是设置全局默认版本
volta install node@14.18.0

# 为一个项目选择节点引擎和包管理器，  这个命令需在项目目录下使用，该命令会记录版本号到 package.json 文件中
# 固定项目的运行时或包管理器
volta pin node@14.18.0

# 从工具链中删除
volta uninstall node@14.18.0

# 查看 volta 的安装的工具目录
volta which <binary>

# 设置当前 用户/shell 用户启动 volta
volta setup

# 运行带有自定义 Node、Yarn、Pnpm、npm 的版本命令
volta run

```



### Nvm

**Nvm（Node.js Version Management）** 是 Nodejs 版本管理工具

```powershell

# 查看已安装的Nodejs
nvm list

# 查看可以安装的版本
nvm ls available

# 切换版本
nvm use 版本号

# 安装版本
nvm install 版本号

# 删除版本
nvm uninstall 版本号

# 可以在项目根目录里记录 node 版本号，
# window 系统下可能不生效
# 在 .nvmrc 文件下记录 node 版本号
# 例如：直接在 .nvmrc文件下写下  v14.16.1
# 使用直接输入在根目录下输入；后面不用跟版本号
num use

```



## TypeScript

TypeScript 是一个以 JavaScript 为基础的语言，TS 不可以像 JS 样直接被浏览器解析。

TS 需要编译成 JS 后才能使用，TS 拓展了 JS 并添加了类型。让 JS 变得更加规范、更严谨、更利于维护。

TS 就相当于 严格模式下的 JS



使用 TS 前需要先安装依赖环境 Node.js 使用里面的 npm 包管理工具安装

```shell

#全局安装 typescript
npm install -g typescript

#使用 将 xxx.ts 文件转换成可以被浏览器解析的 xxx.js 文件
tsc xxx.ts

#时时监听 有修改内容就会自动转换成 js文件
tsc xxx.ts -w  

#查看 typescript 版本号
tsc -v

#生成 tsconfig.json 配置文件
tsc -init

```



#### TypeScript 书写规范：

```js

// 定义 a 的值为 1 类型为 Number 
let a:Number = 1;      

// 定义 b 的值为 hello 类型为 String   一般不这样写(通是赋值和赋值类型)
let b:String = 'hello' 

 // 定义 a 的类型为 Number
let a:Number;        

// 一般是这样写
let a = 1234;			  

// 这样写 TS 会自动判断 b 的类型为 String 并且 b 的类型定义为 String
let b = 'hello'		  


```



#### JavaScript 书写规范：

```js

// 字符串截取
let str = 'http://www.baidu.com/search?value=a'
str = url.split("?")[0]					// 根据问号分组取第一个值；
//str 输出 ['http://www.baidu.com/search']

str.substring(start,end)				// start: 开始值 从0开始计算； end：结束值 从1开始计算
str = str.substring(0,1)				// 从索引值0开始 截取到1位  
//输出 h

str.substr(start,length)				// strat：开始值 从0开始计算； lenght：截取长度
str.substr(0,2)							//从索引值0开始截取两位值
//输出 ht

//数组截取
// slice 既可以截取数组也可以截取字符串， 不会改变原数组而是返回一个新数组。
// splice 只可以截取数组，会改变原数组。
let arr = ['yellow','green','red'];

arr.slice(start,end)				//start：开始值 从0开始； end：结束值 从1开始。 splice()也是一样
str = arr.slice(1, 2)				// 从索引值为1的截取到第2个
// str 输出 ['yellow']


a = [3,2,1];
b = a;
b[0] = 30;
// a 输出 [30,2,1]

//抛出异常
throw new Error("我是一个错误");

//获取 div 的样式
window.getComputeStyle(div)

```



### JavaScript 操作DOM:

```js

document.designMode = 'on'    //页面所有元素可编辑

```





## 防抖和节流：

#### 防抖（Debounicng）

防抖是用于延迟执行某个函数，直到某个连续动作停止触发一段时间后才执行。在连续触发事件时，只有当一定的间隔时间过去后，才会触发该函数执行。这对于处理需等待一段时间后才执行的任务非常有用，比如：搜索框输入、窗口大小调整、按钮点击次数过多等。

```js

//未封装直接使用防抖技术的
let timer = null;
function input () {
    if(timer !== null) {
        clearTimeout(timer)
    }
    timer = setTimeout(() => {
        // 要执行的函数体
        console.log(value)
    },500)
}


// 封装防抖函数
function debounce(fn,delay) {
    const args = arguments;
    let timer;
    if(timer) {
        clearTimeout(timer)
    }
	timer = setTimeout(() => {
        fn.apply(this,args)
    },delay)
}
//用法
const fun = debounce(searchHandle, 100);



/**
 * @desc 防抖函数：一定时间内，只有最后一次执行操作
 * @param {Function} fn 要执行的函数
 * @param {Number} delay 延迟执行毫秒
 */
const debounce = (fn, delay) => {
    let timer;
    return function() {
        let args = arguments;
        if (timer) {
            clearTimeout(timer)
        }
        timer = setTimeout(() => {
            fn.apply(this,args)
        },delay)
    }
}

```



#### 节流（Throttling）

节流是确保函数在一定时间间隔内最多执行一次。它会在指定的时间段内定期执行函数，而不管事件触发的频率有多高。节流适用于需要在连续事件中控制函数执行频率的情况。比如：鼠标移动事件、鼠标滑轮滚动事件等。



```js


//节流
let flag = true;
function scroll() {
    if(flag) {
        setTimeout( () => {
            console.log('hello')
            flag = true
        },500)
    }
    flag = false;
}

//封装节流函数
function throttle(fn, delay) {
    let throttleTimer;
      return function() {
          const context = this;
          const args = arguments;
          if (!throttleTimer) {
              throttleTimer = setTimeout(() => {
                  func.apply(context, args);
                  throttleTimer = null;
              }, 500);
          }
      }
}



/**
 * @desc 节流函数：在一定时间内只触发一次
 * @param {Function} fn 执行函数
 * @param {Number} delay 延迟执行毫秒
 */
let previous = 0;
const throttle = (fn, delay) => {
    let now = new Date();
    if (now - previous > delay) {
        fn();
        previous = now;
    }
}

```





### JS 键盘键值对：

```scss

//键值keycode = 对应的键盘按键
    8 = BackSpace BackSpace
    9 = Tab Tab
   12 = Clear
   13 = Enter
   16 = Shift_L
   17 = Control_L
   18 = Alt_L
   19 = Pause
   20 = Caps_Lock
   27 = Escape Escape
   32 = space space
   33 = Prior
   34 = Next
   35 = End
   36 = Home
   37 = Left
   38 = Up
   39 = Right
   40 = Down
   41 = Select
   42 = Print
   43 = Execute
   45 = Insert
   46 = Delete
   47 = Help
   48 = 0 equal braceright
   49 = 1 exclam onesuperior
   50 = 2 quotedbl twosuperior
   51 = 3 section threesuperior
   52 = 4 dollar
   53 = 5 percent
   54 = 6 ampersand
   55 = 7 slash braceleft
   56 = 8 parenleft bracketleft
   57 = 9 parenright bracketright
   65 = a A
   66 = b B
   67 = c C
   68 = d D
   69 = e E EuroSign
   70 = f F
   71 = g G
   72 = h H
   73 = i I
   74 = j J
   75 = k K
   76 = l L
   77 = m M mu
   78 = n N
   79 = o O
   80 = p P
   81 = q Q at
   82 = r R
   83 = s S
   84 = t T
   85 = u U
   86 = v V
   87 = w W
   88 = x X
   89 = y Y
   90 = z Z
   96 = KP_0 KP_0
   97 = KP_1 KP_1
   98 = KP_2 KP_2
   99 = KP_3 KP_3
 100 = KP_4 KP_4
 101 = KP_5 KP_5
 102 = KP_6 KP_6
 103 = KP_7 KP_7
 104 = KP_8 KP_8
 105 = KP_9 KP_9
 106 = KP_Multiply KP_Multiply
 107 = KP_Add KP_Add
 108 = KP_Separator KP_Separator
 109 = KP_Subtract KP_Subtract
 110 = KP_Decimal KP_Decimal
 111 = KP_Divide KP_Divide
 112 = F1
 113 = F2
 114 = F3
 115 = F4
 116 = F5
 117 = F6
 118 = F7
 119 = F8
 120 = F9
 121 = F10
 122 = F11
 123 = F12
 124 = F13
 125 = F14
 126 = F15
 127 = F16
 128 = F17
 129 = F18
 130 = F19
 131 = F20
 132 = F21
 133 = F22
 134 = F23
 135 = F24
 136 = Num_Lock
 137 = Scroll_Lock
 187 = acute grave
 188 = comma semicolon
 189 = minus underscore
 190 = period colon
 192 = numbersign apostrophe
 210 = plusminus hyphen macron
 211 =
 212 = copyright registered
 213 = guillemotleft guillemotright
 214 = masculine ordfeminine
 215 = ae AE
 216 = cent yen
 217 = questiondown exclamdown
 218 = onequarter onehalf threequarters
 220 = less greater bar
 221 = plus asterisk asciitilde
 227 = multiply division
 228 = acircumflex Acircumflex
 229 = ecircumflex Ecircumflex
 230 = icircumflex Icircumflex
 231 = ocircumflex Ocircumflex
 232 = ucircumflex Ucircumflex
 233 = ntilde Ntilde
 234 = yacute Yacute
 235 = oslash Ooblique
 236 = aring Aring
 237 = ccedilla Ccedilla
 238 = thorn THORN
 239 = eth ETH
 240 = diaeresis cedilla currency
 241 = agrave Agrave atilde Atilde
 242 = egrave Egrave
 243 = igrave Igrave
 244 = ograve Ograve otilde Otilde
 245 = ugrave Ugrave
 246 = adiaeresis Adiaeresis
 247 = ediaeresis Ediaeresis
 248 = idiaeresis Idiaeresis
 249 = odiaeresis Odiaeresis
 250 = udiaeresis Udiaeresis
 251 = ssharp question backslash
 252 = asciicircum degree
 253 = 3 sterling
 254 = Mode_switch 

```