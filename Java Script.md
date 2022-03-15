# Java Script

##### Java Script：简称 js

##### 几个学习前端的库:

  H-ui（admin组件库）、Element-ui（pc端组件库）、Vant（安卓端组件库）、Vue3、jQuery、

 javaScript是一种脚本语言，可以提高用户提高用户体验度。（依托于浏览器）引擎是浏览器Javascript是跨平台的，为什么跨平台？以为依托于浏览器，不依托于操作系统

##### JavaScript更像是一门函数式编程语言。

<script type="text/javascript"><sccript/>           //可以放在body里面也可以放在外边，也可以放在head里面

###### ECMAScript核心  // 隐藏head里面的代码一行
###### DOM文档对象模型 /*....*/隐藏head和css里面的代码全部
###### BOM浏览器对象模型 快捷键Ctrl+/     <!........>在body中隐藏代码

##### 三目运算符也叫三元运算符：  这样写 c = a > b ? a : b ; 如果条件成立就会把
##### 第一个值赋给 c 这就是三目运算符

###### Java引入方式：内部引用；外部引用；行内格式‘

###### 内部引用：<script  type="text/javaScript">    </script>

###### 外部引用：<script src="index.js"></script>可以在head中引用 也可以在body中引用

###### 行内引用：？

######  内部JavaScript，指的是把HTML代码和JavaScript代码放在同一个文件中。

###### 在JavaScript中，每一条语句都是英文分号“;”作为结束符。每一条语句都有它特定的功能。

##### 如果只写了 ；号那就是空语句的意思


##### var a = 10；直接赋值    var声明符   a变量名    = 赋值符  10值     ；语句块结束符号

##### alert  警告；告诫 在JavaScript中意思为弹出框警告的意思     else否则     int整数   parse强制       parseint强制整数

##### alert（）；在网页弹出一个对话框           \n 在谷歌和火狐浏览器中换行

##### \r在IE浏览器中换行。

##### document.write("");基本网页显示的一种语法语法

##### a=1;初始化赋值

##### var a = Number(prompt("请输入一个值"))；弹窗语法

##### 赋值=     右边给左边赋值

#### 变量
##### 在JavaScript中，变量指的是一个可以改变的量。也就是说，变量的值在程序运行过程中是可以改变的
##### 变量由字母、下划线、$或数字组成，并且第一个字母必须是“字母、下划线或$”；
#####   变量不能是系统关键字和保留字

##### 注意：JavaScript的变量名区分大小写，A和a是两个不同的变量。

##### 引用数据类型：对象   数组
##### 数字：10    -10   1.

###### 基本数据类型：数值类型，布尔值类型，字符串类型
###### 特殊数据类型：null，undefined
###### 复合数据类型：数组，对象


##### 数据类型：数值、复合、基本、布尔值（ true、false ）特殊数据类型 null undefined

#### JavaScript标识符（命名规则）
##### 标识符由字母、数字、下划线_、美元符号$、组成
##### 不能以数字开头、不能是系统关键字、严格区分字母大小写、不能以中划线开头、不能包含中划线

##### 标识符（identifier）指的是用来识别各种值的合法名称。最常见的标识符就是变量名。

##### 水仙花数：水仙花数是指一个n位数（n>=3）,他的每个位上的数字的n次冥之和等于它本身。

##### 例如：1^3+5^3+3^3=153     

= 一个等于是赋值
== 两个等于是判值判断关系运算赋是否相等
=== 三个等于是判断类型（全等于）

关系运算符： 小于 <    大于 >    小于等于 <=     大于等于 >=    不等于 !=

逻辑运算符：逻辑&&两者都为真，则为真。逻辑 | | 其中一个为真，则为真。

逻辑！取相反值，本来是真 加入！之后就变成假了

算数运算符：等于 ==     左加 +=      左减 -=       左乘 *=       左除 /=       左

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
while(循环条件：判断布尔值){
	循环体
  	i++；（计步器，是循环趋近于结束）
}

  // ; 代表空语句

//先执行，在判断条件
do{

}while(循环条件)

```

isNaN()判定字母如果是字母返回true，如果不是返回false

###### 短路效应

逻辑&&第一个表达式不成立第二个表达式不运行

逻辑 | | 第一个表达式成立第二个表达式不运行

###### 五大核心浏览器：火狐Firefox   谷歌Google    IE浏览器（InternetExplorer）   苹果浏览器Safai    欧鹏浏览器

##### 分支结构

单分支，双分支，多分支



单分支  if(){ }

双分支  if(){}else{}

多分支  if(){}else if(){}else(){};



break； 结束全部循环

continue；结束本次循环，结束一次循环（直接跳到循环条件的地方）

### switch

一种比 if 读取快，写起来比 if 多     switch只能判断一个值，不能判断范围，而

#### if 能判断范围

##### 例如：

```javascript
var a= 1 ；
switch(a){
 case1:
 document.write（“a=”+a）;
 break; // 注意：没有break；的时候从没有break；往下的都会输出一遍

 case2:
 document.write（“a=”+a）;
 break;

 case3:
 document.write（“a=”+a）;
 break;

 default:
 document.write(a);
 break;
}

 //for 循环的执行顺序 1‐2‐3‐5‐6‐7‐9‐8‐7‐9‐8‐7‐4‐10‐11
 for( 2 ; 3 ; 4 ){ 再来到这个循环里，重新循环
     for( 6 ; 7 ; 8 ){
      9  如果这里有break; 那他就直接结束只一个循环
     }
    10
 }
 11

 do{
 循环体
 }while()
// 先执行，再判断条件 while先判断条件再执行代码 其实while和do while是一样的
//强制转化为整数 parseInt（）
//判定字符串 如果是字符串返回 true 如果不是返回 false isNaN（）
//强制转化为小数 parseFloat（）
函数 function（）{
	 执行体
 	}
}

if(a% 2 == 0 ){
 //取余
}
```
##### window.onload   告诉计算机等到页面加载完了以后在执行的代码

计时器  setTimeout（"需执行的函数",1000毫秒）；意思过多少秒执行一次的

计时器  setInterval   ("需要执行的函数"，时间毫秒)；意思每过多少时间执行一次的代码；

手动结束的话用  clearTimeout(id)清除timeout的     clearInterval(id)清除interval的

##### 数组    

a= [ x ] [ y ]    或 var a [ x ] =1;

下标减一   下标是从零开始的


##### eval（"  "）把里面的字符串当代码执行

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
document.onkeydown(e){
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
 var list = [ 45 ,  4 ,  6 ,  1 ,  14 ,  55 ,  10 ,  9 ];
 function sort(list){
 for (i =  0 ; i <  5 ; i++) {
     for (j =  0 ; j <  7  ‐ i; j++) {
         if (list[j] < list[j +  1 ]) {
             b = list[j];
             list[j] = list[j +  1 ];
             list[j +  1 ] = b;
         }
     }
 }
     for(k in list){
	     document.write(list[k]+"<br/>")
     }
 }
 sort(list);
```
#### 递归：

1 . 假设递归函数已经写好

2 . 寻找递推关系

3 . 将递推关系的结构转换为递归体

4 . 将临界条件加入到递归体中



```js
//简单的递归
if (n == 1) return 
   return sum(n ­ 1) + n
 }

// 一个简单的阶乘函数
var f = function(x){
    if (x ===  1){
     	return  1 ;
     } else{
    	return x * f(x ‐  1 );
	 }
 }

// 递归方法 ：
function fib(n) {
	 if (n ===  1  || n ===  2 ) return n ‐  1  return fib(n ‐  1 ) + fib(n ‐  2 )
 }
  console.log(fib( 10 )) 
 //非递归方法 
 function fib(n) {
     let a =  
     let b =  
     let c = a + b
     for (let i =  3 ; i < n; i++) {
         a = b b = c c = a + b
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

getDate() 以数值返回天（1-31）
getDay() 以数值获取周名（0-6）
getFullYear() 获取四位的年（yyyy）
getHours() 获取小时（0-23）
getMilliseconds() 获取毫秒（0-999）
getMinutes() 获取分（0-59）
getMonth() 获取月（0-11）
getSeconds() 获取秒（0-59）
getTime() 获取时间（从 1970 年 1 月 1 日至今）
```


## Node.js:

简单的说 Node.js 就是运行在服务端的 JavaScript。

Node.js 是一个基于Chrome JavaScript 运行时建立的一个平台。

Node.js是一个事件驱动I/O服务端JavaScript环境，基于Google的V8引擎，V8引擎执行Javascript的速度非常快，性能非常好。

### Node.js 安装包及源码下载地址为：https://nodejs.org/en/download/。

```js
 // 创建一个应用
 const http = require("http"); //引入一个 http 模块
 const fs = require("fs"); //引入一个 fs 模块
 const url = require("url"); //引入一个 url 模块

 http.createServe(function(request,response){ 
 response.setHeader("Content‐type","text/html;charset=utf8;"); //设置 响应 是 设置内容编码格式
     response.wirteHead 第一个参数是( 200 ,{"Content‐type" 设置状态码 :"text‐plain;charset=utf8;"}) //也 转换
     let.query  urlData 是接收= urlGET值.parse true (是执行request.url,true).query; //把 url GET 传的值格式 加文件名
     let txtData  加上Sync=意思是执行同步 fs.readFileSync('test.txt'); //读取文件 参数是文件名 或 路径 参数是值，如果没有该文件会创建该文件，如果有内容则会覆盖。
     fs.wirteFile("test.txt",value); //写入文件 第一个参数和读取文件一样 第二个
	 response.end('hello world') //相应内容
 }).listent( 8888 ) //设置端口号
```
##### Node Koa2框架： 封装原生代码的 API

```sh
#Node 安装Koa2 安装完成 不会自带 node_module 需要手动安装一下
npm i
#安装koa2
npm i ‐g koa‐generator      	# 使用 npm 包管理工具 安装 i 是 install 的缩写 ‐g 是全局

#查看 版本
koa2 ‐‐version

#创建项目
koa2 文件名称

#打开项目
koa2 run dev 项目名称
```

#### Node mon 工具插件：nodemon是一种工具，可以自动检测到目录中的文件

##### 更改时通过重新启动应用程序来调试基于node.js的应用程序。

```sh
#安装 nodemon
npm i ‐g nodemon                   #使用 npm 安装 ‐g 全局的 nodemon

#使用
nodemon 文件名或路径名加文件名       # 使用 nodemon 打开 node 服务

#nodemon 命令
rs 重启一下 是 restart 的缩写
```
##### Node Token：

```js
// 安装 jwt jsonwebtoken
npm install jsonwebtoken

//引用 jsonwebtoken
const jwt = require('jsonwebtoken');

// 登录成功 生成token
const token = jwt.sign({
	time:Date now(),
	timeout:Date now() +  60000 ,
	用户信息 等等
},'token'),

// 解析验证token
let token = ctx.request.headers['token'];
const token = jwt.verify(token,'token');
```
##### Node   Mysql连接数据库：

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
var query = (Sql)=>{
return new Promise((resolve,reject) => {
        connection.query(Sql,function (err, result) {
            if(err){
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

```js
//安装 WebScoket
npm install ws

//引入使用
const ws = require("ws");

//客户端使用
//连接服务器
	var ws = new WebSocket("ws:localhost:888");
	//打开连接
	ws.onopen = function(e){
		console.log("客户端：与服务器的连接已打开");
	};
	//接收服务器端发的消息
	ws.onmessage = function(e){
		console.log(e.data)
		//document.getElementById("list").innerHTML += "<li>"+e.data+"</li>"
	}
	//触发事件 发送消息
	function sendMessage(){
		var message = document.getElementById("message").value;
		// console.log(message);
		ws.send(message);
	};


//服务器端使用如下
//创建websocket服务
var WebSocketServer = require("ws").Server;

//设置端口号
wss = new WebSocketServer({port:888});

//查看 所有客户端
console.log(wss.clients )

//连接客户端
wss.on("connection",function (ws){
	console.log("服务器端：客户端已连接");

	//接收客户端的消息
	ws.on("message",function(message){
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





#### Node js  Joi：JavaScript对象的规则描述语言和验证器。

```js
const Joi = require('joi'); //引入joi模块
Joi.string()/Joi.number() //定义只能是字符串类型/数字类型
Joi.alphanum() //只能是字母字符串或数字字符串
Joi.max()/Joi.min() //限制最大字符串长度/限制最小字符串长度
Joi.required() //此属性必填
Joi.error() //定义错误信息
Joi.regex() //接受一个字符串规则验证
Joi.integer() //必须是整数
//对象验证
Joi.validate({ username: 'abc', birthyear:  1994  }, schema);
```


#### Node pm2

**说明：**是一个守护进程管理器，不会占用一个终端，而是在后台运行 js。



**用法：**

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





#### JavaScript 小语句：

```js
//字符串截取
str = url.split("?")[ 0 ] //根据问号分组取第一个值；
//数组截取
arr = ['yellow','green','red'];
str = arr.slice( 1 , 2 ) //从下标值为  1  的截取 截取到第  2  个

a = [ 3 , 2 , 1 ];
b = a;
b[ 0 ] =  30 ;
console.log(a);
//输出结果为 [30,2,1]

//抛出异常
error = (()=>{
    throw new Error("抛出异常");
})();
```



### JavaScript 操作DOM:

```js
document.designMode = 'on'    //页面所有元素可编辑
```

