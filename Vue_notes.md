# Vue笔记

#### 介绍

Vue.js（读音 /vjuː/, 类似于 view） 是一款构建用户界面的 JavaScript 框架。它基于 HTML、CSS 和 JavsScript 构建，并提供了一套声明式、组件化的模型，帮助我们高效的开发用户界面。Vue 只关注视图层， 采用自底向上增量开发的设计。

#### 安装使用

**通过Node.js包管理工具创建使用**

```sh

# npm
npm create vue@latest

# pnpm 
pnpm create vue@latest

# yarn v2+
yarn create vue@latest

# yarn v4.11
yarn dlx create-vue@latest

# bun
bun create vue@latest


# 安装依赖
npm install

# 本地开发环境 启动项目
npm run dev

# 构建生产环境
npm run build

# yarn 安装依赖
yarn 

# yarn 启动
yarn dev

# yarn 构建
yarn build
```



**通过CDN创建**

```html

<!-- 通过script标签引入vue直接使用 -->
<script src="https://unpkg.com/vue@3/dist/vue.global.js"></script>

<div id="app">
	{{ message }}
</div>

<script>
	const { createApp, ref } = Vue
    
    createApp({
        setup() {
            const message = ref('Hello world')
            return {
                message
            }
        }
    }).mount('#app')
</script>

```





### Vue SEO 优化方案

**SEO（Search Engine Optimization）** 

汉译为搜索引擎优化。是一种方式：利用搜索引擎的规则提高网站的在有关搜索引擎内的自然排名。目的是让其在行业内占据领先地位，获得品牌效益。



**预渲染 SPA：** 预渲染不仅可以优化 SEO 还可以解决首屏加载白屏问题。  prereender-spa-plugin

**静态化：** 静态化是 Nuxt.js 的另一种方式，页面速度加载很快。在 Nuxt.js 中执行 generate 静态化打包时，动态路由会被忽略

**SSR 服务端渲染：**  服务端渲染就是在服务器发送到浏览器前，就将页面渲染上。

**Phantomjs：** 是一个基于 webkit 内核的无头浏览器，即没有UI界面，使用 Phantomjs 针对爬虫做处理。



<img src="./img/seo.jpg"/>

#### Vue模板语法：

Vue 使用了基于 HTML 的模板语法，允许开发者声明式地将 DOM 绑定至底层 Vue 实例的数据。

数据绑定最常见的形式就是使用 {{ }} 的文本插值{{...}} 标签的内容将会被替代为对应组件实例中 **message** 属性的值，如果 **message** 属性的值发生了改变，{{...}} 标签内容也会更新。如果不想改变标签的内容，可以通过使用 **v-once** 指令执行一次性地插值，当数据改变时，插值处的内容不会更新。
``` html

<span v-once>这个将不会改变: {{ message }}</span>

```

例如：

``` html js

<div id="hello-vue" class="demo">  
    {{ message }}
</div>
<script> 
    const HelloVueApp = {  
        data() {    
            return {  
                message: 'Hello Vue!!'     
            }
        }
    }
    Vue.createApp(HelloVueApp).mount('#hello-vue') 
</script>

```

#### 使用 v-html 指令用于输出 html 代码

例如
``` html js

<div id="example1" class="demo"> 
    <p>使用双大括号的文本插值: {{ rawHtml }}</p>
    <p>使用 v-html 指令: <span v-html="rawHtml"></span>
    </p>  
</div>
<script>
    const RenderHtmlApp = {
        data() {  
            return { 
                rawHtml: '<span style="color: red">这里会显示红色！</span>'       
            }
        }
    }
    Vue.createApp(RenderHtmlApp).mount('#example1')
</script> 
<!-- v-bind 指令用于绑定一个属性 -->
<div v-bind:id="dynamicId"></div>

```
#### Vue.js 都提供了完全的 JavaScript 表达式

表达式会在当前活动实例的数据作用域下作为 JavaScript 被解析。有个限制就是，每个绑定都只能包含单个表达式，所以下面的例子都不会生效:
``` html

<!--  这是语句，不是表达式：-->
{{ var a = 1 }}

<!-- 流控制也不会生效，请使用三元表达式 --> 
{{ if (ok) { return message } }}

```
##### 指令：

指令是带有 v- 前缀的特殊属性。

指令用于在表达式的值改变时，将某些行为应用到 DOM 上。如下例子：
``` html js

<div id="app">
    <p v-if="seen">现在你看到我了</p>  
</div>
<script> 
    const app = { 
        data() { 
            return {
                seen: true /* 改为false，信息就无法显示 */ 
            }
        }
    }
    Vue.createApp(app).mount('#app')  
</script>

```
这里， v-if 指令将根据表达式 seen 的值( true 或 false )来决定是否插入 p 元素。

另外还有其它很多指令，每个都有特殊的功能。例如，v-for 指令可以绑定数组的数据来渲染一个项目列表。

##### 参数：

参数在指令后以冒号指明。例如， v-bind 指令被用来响应地更新 HTML 属性：

在这里 href 是参数，告知 v-bind 指令将该元素的 href 属性与表达式 url 的值绑定。

另一个例子是 v-on 指令，它用于监听 DOM 事件：
```html

<!-- 完整语法 -->
<a v-on:click="doSomething"> ... </a>

<!-- 缩写 --> 	
<a @click="doSomething"> ... </a>  

<!-- 动态参数的缩写 (2.6.0+) -->
<a @[event]="doSomething"> ... </a>

```

##### Vue条件语句：

v-if=" 条件 "  

v-else-if=" 条件 "

v-else

v-show=" 条件 "

v-show 与 v-if 的区别：

​					**相同点：v-if与v-show都可以动态控制dom元素显示隐藏**

​					**不同点：v-if显示隐藏是将dom元素整个添加或删除，而v-show隐藏则是为该元素添加css--display:none，dom元素还在。**



**v-once的作用: 只渲染元素和组件一次。随后的重新渲染，元素/组件及其所有的子节点将被视为静态内容并跳过。这可以用于优化更新性能。**





**Vue循环语句：**

​			v-for 指令需要以 **site in sites** 形式的特殊语法， sites 是源数据数组并且 site 是数组元素迭代的别名。

例如：
``` html

<div id="app">
    <ol>  
        <li v-for="site in sites">
            {{ site.text }}
        </li> 
    </ol>
</div> 
<script> 
    const app = {  
        data() {   
            return {
                sites: [  
                    { text: 'Google' },
                    { text: 'Runoob' },   
                    { text: 'Taobao' }  
                ]
            }
        }
    }
    Vue.createApp(app).mount('#app') 
</script>

```
v-for 还支持一个可选的第二个参数；也支持第三个参数

第一个参数是值，第二个是键名，第三个是索引名。



#### Vue组件： 

在这里，可以将 #app 元素认为是父组件的模板，它就是起着父组件的作用，

<hello word /> 为子组件。

数据是通过在父组件中的 <input /> 获得，然后通过 子组件的 v-bind 方法，传给了子组件。

此时子组件 <hello wrod /> 内部获得了 mymessage 数据，将其通过模板渲染到页面上。

template 属性只是作为一个模板，显示数据，本身不是组件。

简而言之，子组件在父组件的 template 属性或者是模板中。此处 整个 #app 元素作为父组件的模板， <hello wrod/> 在其中渲染，所以 <hello word /> 为子组件。



##### 父组件向子组件传值:

一般会在子组件里面定义props来做接收，这是比较常见的情况

**父组件：**

``` vue

<template>  
<div>
    <div>我是父组件</div>  
    <div>我发送给第一个组件的信息是:{{msg}}</div> 
    <div>
        <div id="child1">    
            <ChildOne :msg="msg" />     
	    </div>   
    </div> 
</div>
</template> 
<script> 
    import ChildOne from "../components/children1"; 
    import ChildTwo from "../components/children2"; 
    export default {  
        components: {   
            ChildOne,
            ChildTwo  
        },  
        data() { 
            return { 
                msg: "我是父组件，我给你发消息",     
            };
        }
    };
</script>

```
可以看到我在第一个子组件上面传入了一个msg,那么在子组件上就需要定义一个msg用来接收传进来的参数

**子组件：**
``` vue

<template> 
<div>  
    <div id="title">我是第一个子组件</div>   
    <div>我接受到的父组件的消息是：{{msg}}</div>
</div>
</template>
<script> export default {
        props: {    
            msg: {   
                type: String
            }
        }
    }
</script>

```
##### 子组件向父组件传值：

这时候就需要利用vue中的$emit将想要传递的值通过函数的形式传出，在父组件接收

this.$emit(arg1,arg2) arg1:方法名字，arg2:要传出的值



**子组件**

``` vue

<template>
<div>
    <div id="title">我是第二个子组件</div>    
    <div>我要发送给父组件的值：{{msg}}</div>
    <button @click="toParent">向父组件发送信息</button> 
</div>
</template>
<script> 
    export default {  
        data() {  
            return {   
                msg: "我是第二组件，我要给父组件传值", 
            };
        },
        methods: {   
            toParent() { 
                this.$emit("toParent", this.msg); 
            }
        }
    };
</script>

```
我在button上绑定了一个点击事件，函数里面传出了一个方法名为toParent的方法，这时候我们就要去父组件接收这个函数，它会带一个返回值，这个返回值就是我们需要从子组件传的值。



**父组件**

``` vue

<template>
<div>   
    <div>我是父组件</div>   
    <div>我即将接收第二组件传值是：{{child2Msg}}</div>   
    <div>    
        <div id="child2"> 
            <ChildTwo @toParent="getMag" />   
	    </div>  
    </div>  
</div>
</template> 
<script>
    import ChildOne from "../components/children1"; 
    import ChildTwo from "../components/children2";
    export default {  
        components: {   
            ChildOne, 
            ChildTwo 
        },
        data() {  
            return {  
                child2Msg: "" 
            };
        },
        methods: {   
            getMag(msg) {     
                this.child2Msg = msg;     
            }
        }
    };
</script>

```
<span style="font-weight:bold;color:red;"> 组件（Component）是 Vue.js 最强大的功能之一。</span>

组件可以扩展 HTML 元素，封装可重用的代码。

组件系统让我们可以用独立可复用的小组件来构建大型应用，几乎任意类型的应用的界面都可以抽象为一个组件树：



每个 Vue 应用都是通过用 createApp 函数创建的，传递给 createApp 的选项用于配置根组件。当我们挂载应用时，该组件被用作渲染的起点。一个应用需要被挂载到一个 DOM 元素中。
``` html

<!-- 实例：我们将 Vue 应用挂载到 -->
<div id="app"></div> <!-- 应该传入 #app：-->

<script>
const RootComponent = { /* 选项 */ } 		
const app = Vue.createApp(RootComponent) 		  
const vm = app.mount('#app')


//注册一个全局组件语法格式：
const app = Vue.createApp({...}) 			
app.component('my-component-name', {})

</script>
//一个简单Vue组件的实例：
<div id="app">   
    <runoob></runoob>
</div> 
<script> 
    // 创建一个Vue 应用 
    const app = Vue.createApp({}) 
    // 定义一个名为 runoob的新全局组件 
    app.component('runoob', { 
        template: '<h1>自定义组件!</h1>'
    }) 
    app.mount('#app')  

//接下来我们再注册一个 button-counter 组件，在每次点击后，计数器会加 1:
// 创建一个Vue 应用 
    const app = Vue.createApp({}) 
// 定义一个名为 button-counter 的新全局组件 
    app.component('button-counter', { 
        data() {  
            return {  
                count: 0  
            }
        },
        template: `   <button @click="count++">    点了 {{ count }} 次！   </button>`
    })
    app.mount('#app') 
</script>

```
组件可以重复使用；



#### Vue 修饰符：
修饰符是以半角句号 . 指明的特殊后缀，用于指出一个指令应该以特殊方式绑定。例如，**.prevent** 修饰符告诉 v-on 指令对于触发的事件调用**event.preventDefault()**：
``` html

<form v-on:submit.prevent="onSubmit"></form>

```
##### 事件修饰符：

在事件处理程序中调用 event.preventDefault() 或 event.stopPropagation() 是非常常见的需求。尽管我们可以在方法中轻松实现这点，但更好的方式是：方法只有纯粹的数据逻辑，而不是去处理 DOM 事件细节。

为了解决这个问题。vue.js 为 v-on 提供了 **事件修饰符。** 修示符是由点开头的指令后缀来表示的。



*使用修饰符时，顺序很重要；相应的代码会以同样的顺序产生。因此，用 `v-on:click.prevent.self` 会阻止**所有的点击**，而 `v-on:click.self.prevent` 只会阻止对元素自身的点击。*

``` html

.stop   <!-- 阻止单击事件继续传播 -->
<a v-on:click.stop="doThis" ></a>

.prevent  <!--提交事件不再重载页面 -->
<form v-on:submit.prevent="onSubmit" ></form> 
<form v-on:submit.prevent ></form> 

<!--修饰符可以连串-->
<form v-on:click.submit.prevent="onSubmit" ></form>

<!--只有修饰符 -->

.captrue <!-- 添加事件监听器时使用事件捕获模式  即内部元素出发的事件先在处理，然后才交由内部元素进行处理 -->
<div v-on:click.capture="doThis" >...</div>

.self <!--只当event.target是当前元素自身时触发处理函数  即使事件不是从内部元素触发的-->
<div v-on:click.self="doThis"></div>

.once <!--点击事件只会触发一次-->
<a v-on:click.once="doThis" ></a>

.passive <!--Vue 还对应 addEventListener 中的 passive 选项提供了 .passive 修饰符-->
<!--滚动事件的默认行为（即滚动行为）将会立即触发-->
<!--而不会等待 onScroll 完成-->
<!--这其中包含 event.preventDefault() 的情况-->
<div v-on:click.scroll.passive="onScroll" ></div>

<!--
这个 .passive 修饰符尤其能够提升移动端的性能。
不要把 .passive 和 .prevent 一起使用，因为.prevent将会被忽略，同时浏览器可能会向你展示一个警告。请记住，.passive会告诉浏览器不想被阻止事件的默认行为。
-->

```
##### 按键修饰符：

在监听键盘事件时，我们经常需要检查详细的按键。Vue允许 v-on 在监听键盘事件时添加按键修饰符：

```html

<!--只有在 key 是 Enter 时调用 vm.submit()-->
<input v-on:keyup.enter="submit" />

<!--您可以直接将 KeyboardEvent.key 暴露的任意有效按键名转换为 kebab-case 来作为修饰符。-->
<input v-on:keyup.page-down="onPageDown" />
<!--在上述示例中，处理函数只会在 $event.key 等于 PageDown 时会被调用。-->

<!--keyCode attribute 也是允许的-->
<input v-on:keyup.13="submit" />

<!--为了在必要的情况下支持就浏览器，Vue提供了绝大多数常用的按键码的别名-->
.enter
.tab
.delete <!--捕获“删除”和“退格”键-->
.esc
.space
.up
.down
.left，
.right
<!--有一些按键（.esc以及所有的方向键）在IE9中有不同的 key 值，如果你想支持IE9，这些内置别名应该是首选-->

```

你还可以通过全局的 config.keyCode 对象[自定义按键修饰符别名](https://cn.vuejs.org/v2/api/#keyCodes)：

```js

//可以使用 'v-on:keyup.f1'
Vue.config.keyCode.f1 = 112

```



#### Js本地储存localStorage:

一.简介

　　localStorage会可以将第一次请求的数据直接存储到本地，这个相当于一个**5M**大小的针对于前端页面的数据库

　　 ——注意：在**IE8**以上的IE版本才支持localStorage这个属性。localStorage属于**永久性存储**，如果存储内容多的话会消耗内存空间，会导致页面变卡。

 

二.具体使用方式如下：
``` js

// localStorage - 没有时间限制的数据存储 　　
var arr=[1,2,3];
localStorage.setItem("temp",arr);           //存入 参数： 1.调用的值 2.所要存入的数据 
console.log(localStorage.getItem("temp"));  //输出

//清空 localStorage
localStorage.clear(); 

//删除键值对
localStorage.removeItem("arr");　　

//注意：存入的数据只能以 字符串 形式存入。

```
三.提供转JOSN数据方法：
```json

//JSON对象转JSON字符串
let obj = {"a": 1,"b": 2};
    obj = JSON.stringify(obj); //转化为JSON字符串
　　localStorage.setItem("temp2", obj);
　　//JSON字符串转JSON对象
　　obj = JSON.parse(localStorage.getItem("temp2"));

```



#### 生命周期钩子函数：

beforeCreate：创建之前状态

created：创建完成状态

beforeMount：挂载之前状态

mounted：挂载结束状态

beforeUpdate：数据更新之前状态

updated：数据更新完成状态

beforeDestroy：销毁之前状态

destroyed：销毁之后状态

![img](https://cn.vuejs.org/images/lifecycle.png)

## VueX状态管理：

**概念**：Vuex 是一个专为 Vue.js 应用程序开发的状态管理模式。它采用集中式存储管理应用的所有组件的状态，并以相应的规则保证状态以一种可预测的方式发生变化。

**应用场景**：Vue多个组件之间需要共享数据或状态。

Vuex有几个核心概念：State、Getters、Mutations、Actions、Modules。

 <img src="img/flow.png"/>

State：存储状态数据

Getters：从状态数据派生数据，相当于State的计算属性。（加工state成员给外界）

Mutations：存储用于同步更改状态数据的方法，默认传入的参数为state。（state成员操作）

Actions：存储用于异步更改状态数据，但不是直接更改，而是通过触发Mutation方法实现，默认参数为context。（异步操作）

Modules：Vuex模块化。（模块化状态管理）

<img src="img/vuex.png"/>



### vuex 用法：

```js

//全局注册 在main.js中
import App from './App'
import store from '封装的state.js'

const app = new Vue({
    store,
    ...App
})

//在组件中使用
this.$store.state.data = '新值'

//在state.js中封装
import vuex from "vuex"
export default Vuex.Store({
    state:{
        //状态 数据
    },
    getters:{
        //计算sate派生数据
    },
    mutations:{
    	//同步修改state数据
	},
    actions:{
        //可以异步提交mutations
    },
    modules{
       //模块化管理vuex
	},
})

```







#### 混入数据：

``` js

// 全局注册 在main.js里
import mixin from './mixin/mixin.js' 
Vue.mixin(mixin) 

// 局部注册 在其他vue页面
import mixin from './mixin/mixin.js'
mixins: [mixin]

```
#### 路由守卫：
``` js

router.beforeEach((to, from, next) => {
    console.log(to, from);
    next() 
})
router.afterEach((to, from) => {
    console.log(to, from);
})

```
#### 路由跳转：
``` js

this.$router.push("/about"); 
this.$router.push({  
    name: "About", 
    query: {  
        id: 123  
    }
})
this.$router.push({  
    name: "About",
    params: { 
        id: 123 
    }
})

// 接受路由跳转的值
this.$route.params 
this.$route.query 
this.$router.replace("/about")
this.$router.go(n); //n 1 || n-1

```
``` vue

<!-- 标签使用 -->
<router-link :to="{ name: 'About', query: { id: 123 } }">Query跳转 </router-link>
<router-link :to="{ name: 'About', params: { id: 123 } }">Params跳转</router-link>

```
#### 插槽，具名插槽：
``` vue

<slot></slot>
<slot name="t1"></slot>
<template #t1>haha</template>

```
##### $forceUpdate()的作用：

迫使 Vue 实例重新渲染。注意它仅仅影响实例本身和插入插槽内容的子组件，而不是所有子组件。调用强制更新方法this.$forceUpdate()会更新视图和数据，触发updated生命周期。

##### $nextTick()：

将回调延迟到下次 DOM 更新循环之后执行。在修改数据之后立即使用它，然后等待 DOM 更新。它跟全局方法 Vue.nextTick 一样，不同的          是回调的 this 自动绑定到调用它的实例上。



**nextTick(); 实现思路：**

1. 准备一个任务队列，可以是数组或是微任务队列
2. 封装一个函数，接受回调函数作为参数
3. 在这个函数内部，把回调推入任务队列
4. 在当前调用栈执行完后，从任务队列中弹出函数执行次数

```js

// 实现代码
let callbacks = [];
function flusCallbacks() {
    callbacks.forEach(cb => cb());
    callbacks = [];
}
function $nextTick(cb) {
    callbacks.push(cb);
    queuMicrotask(flusCallbacks);
}

```



#### $ref：

ref 被用来给元素或子组件注册引用信息。引用信息将会注册在父组件的 $refs 对象上如果在普通的 DOM 元素上使用，引用指向的就是 DOM 元素；如果用在子组件上，引用就直向子组件

```html

<p ref='p' > </p>
this.$refs.p     <!--- 这个就是DOM元素 -->

<child-components ref="child"> </child-components>
this.$refs.child  <!-- 而这个就是指向子组件 -->

```



#### 过滤器：
``` js

// 局部过滤器
filters: { 
    setText(res) {   
        if (!res) {  
            return 123; 
        }
        return res  
    },
},
    
// 全局过滤器 
    Vue.filter("capitalize", function(res) {
        if (!res) {  
            return 123;
        }
        return res;
    });
// 批量注册全局过滤器 
// 全局过滤器 
import * as filters from "./filters"; 
Object.keys(filters).forEach((key) => { 
    Vue.filter(key, filters[key]);
});

```


### Axios：

易用、简洁且高效的http库

``` js

// Axios 是一个基于 promise 的 HTTP 库，可以用在浏览器和 node.js 中。 一般应用于，前后端通讯 
// vue 使用 npm 安装 axios 
npm install axios
npm install --save axios vue-axios

//引用&使用 
axios import axios from 'axios'
import VueAxios from 'vue-axios'
Vue.use(VueAxios,axios)

//GET请求传参数
this.axios.get("https://api.datoukang.top/api",{
 params:{
 	   id:1
   }
}).then((response)=>{
          console.log(response)
})

//POST请求传参数
this.axios.post("https://api.datoukang.top/api",{
    id:1
}).then((response)=>{
    console.log(response)
})

//拦截器 
//请求之前执行 
axios.interceptors.request.use(
    config => {
        config.data = "data";    
        config.headers = {   
            'Content-Type': 'application/x-www-form-urlencoded'
        }
        return config;
    },
    error => {  
        return Promise.reject(error);  
    } 
);

//请求之后执行 
axios.interceptors.response.use(response => {  	
    //请求成功后得到的数据    
    return response 
}, err => {    
    if (err && err.response) {
        //err.response.status
    } else { 
        //连接到服务器失败    
    }
    return Promise.resolve(err.response)
})

```
##### Axios 封装：
``` js

// Promise 
function test() { 
    return new Promise((resolve, reject) => {
        //当异步代码执行成功时，我们才会调用resolve(...), 当异步代码失败时就会调用reject(...)  
        setTimeout(() => {      
            resolve("哈哈哈哈");    
        }, 2000);  
    });
} 
async function helloAsync() { 
    var x = await test();
    return x; 
}
helloAsync().then((v) => {  
    console.log(v);
});
//axios.defaults.timeout = 5000; 规定请求超时的时间 
//axios.defaults.baseURL = ''; 配置域名
try { 
    console.log(msg);
} catch (error) { 
    console.log(123); 
}

```
##### 自定义指令：

第一个参数是指令名称，第二个参数是钩子函数

 钩子函数有：

- **bind**：只调用一次，指令第一次绑定到元素时调用。在这里可以进行一次性的初始化设置。
- **inserted**：被绑定元素插入父节点时调用 (仅保证父节点存在，但不一定已被插入文档中)。
- **update**：所在组件的 VNode 更新时调用，但是可能发生在其子 VNode 更新之前。指令的值可能发生了改变，也可能没有。但是你可以通过比较更新前后的值来忽略不必要的模板更新 (详细的钩子函数参数见下)。

**bind** 和 **inserted** 

共同点：dom 插入会调用，bind 在 inserted 之前。

不同点：bind 时父节点为 null ，inserted 时父节点存在。

bind 是在 dom 树绘制之前调用 ；inserted 是在 dom 树绘制后调用



**全局注册：**
``` js

// 注册一个全局自定义指令 
v-focus Vue.directive('focus', { 
    // 当绑定元素插入到 DOM 中。  
    inserted: function (el) {
        // 聚焦元素    
        el.focus()
    }
})

//局部注册： 
directives: {
    focus: {
        // 指令的定义    
        inserted: function (el) {
            el.focus()
        }
    }
}

```
使用如下：
``` html

<input v-focus>

```
#### Vue-cli脚手架：

  Vue CLI 是一个基于 Vue.js 进行快速开发的完整系统，脚手架顾名思义就是搭建工程的一个工具，脚手架有很多，vue-cli是其中的一种。用来帮助快速的搭建vue的开发环境。



在安装之前需要安装node.js

``` shell

#安装：
npm install -g @vue/cli 
#或
yarn global add @vue/cli 

# 升级: 
npm update -g @vue/cli 
#或
yarn global upgrade --latest @vue/cli 

#图形化创建 vue 项目 
vue ui 

#默认配置 运行项目指令
npm run serve      #在项目 根目录 cmd  

#默认配置 打包项目指令
npm run build      # 会在根目录生成一个 dist 文件夹

```
## Vue3 Setup():

在 setup() 内部，this 不是该活跃实例的引用，因为 setup() 是在解析其它组件选项之前被调用的，所以 setup() 内部的 this 的行为与其它选项中的 this 完全不同。这使得 setup() 在和其它选项式 API 一起使用时可能会导致混淆。

``` js

setup(props,context,) {
    //props 是响应式的，不能使用 ES6 解构,    
    //如果需要解构 prop，可以通过使用 setup 函数中的 toRefs 来安全地完成此操作     c
    onst { title } = toRefs(props) 
    console.log(title.value)
}

```



### Vue Keep-alive

1. 一般结合路由和动态组件一起使用，用于缓存组件；
2. 提供 include 和 exclude 属性，两者都支持字符串或正则表达式，include 表示只有名称匹配的组件会被缓存 exclude 表示任何名称匹配的组件都不会被缓存，其中 exclude 的优先级比 include 的高；
3. 对应两个钩子函数 activated 和 deactivated，当组件被激活时，触发钩子函数 activated，当组件被移除时，触发钩子函数 deactivated 。

```vue

<keep-alive>
	<!-- 区域内的值会缓存 -->
</keep-alive>

```



### Vue Cli Watch：

侦听器

```js

watch: {
   //监听 路由
  "$route"(e){
     console.log(e);
   }
}

```



### Vue 导出引入：

**export default：** vue 前端导出 用 import .. from 引入；

**module.export:** node 导出模块 用 require() 引入；



#### 封装接口：

封装一个 request.js 方法



### 运行打包后的 vue 项目：

```shell

#安装 serve
npm install serve -g

#使用 serve
serve 打包后的文件 -s

```





# Nuxt

#### 介绍

Nuxt 的目标是以出色的开发者体验为核心，使 Web 开发变得更直观和高效。vue 用来实现 SSR（服务端渲染）的，为了使 SEO 优化更好的。一个基于 vue 的框架



#### 安装使用

使用模板仓库官方文档里的命令创建不行，只能拉去模板仓库

```sh

# 直接从我的 gitee 拉取
git clone https://gitee.com/datoukang/nuxt3-app.git

# 然后安装依赖包
# 要求node版本 >= 18.0.0
yarn install

pnpm install

npm install

bun install

# 运行  除了 yarn 命令不太一样其它一样
npm run dev

yarn dev

# 打包构建
npm run build

yarn build

# 本地预览
npm run preview

yarn preview

```

#### 打包部署