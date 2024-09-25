# jQuery

#### 介绍

jQuery 是一个快速、小型且功能丰富的 JavaScript 库。它通过可在多种浏览器中运行的易于使用的 API 使 HTML 文档遍历和操作、事件处理、动画和 Ajax 等操作变得更加简单。

#### jQuery与原生态的JS代码不可弄混

**jQuery事件：**

语法写法：

``` js

//回调函数
$("ID或元素").函数 ( ) ,function ( ) { }
$("p").click(function() {
	// 动作触发后执行的代码!!
})

```

### jQuery 事件方法 参考手册:

| 方法                                                         | 描述                                                         |
| :----------------------------------------------------------- | :----------------------------------------------------------- |
| [bind()](https://www.runoob.com/jquery/event-bind.html)      | 向元素添加事件处理程序                                       |
| [blur()](https://www.runoob.com/jquery/event-blur.html)      | 添加/触发失去焦点事件                                        |
| [change()](https://www.runoob.com/jquery/event-change.html)  | 添加/触发 change 事件                                        |
| [click()](https://www.runoob.com/jquery/event-click.html)    | 添加/触发 click 事件                                         |
| [dblclick()](https://www.runoob.com/jquery/event-dblclick.html) | 添加/触发 double click 事件                                  |
| [delegate()](https://www.runoob.com/jquery/event-delegate.html) | 向匹配元素的当前或未来的子元素添加处理程序                   |
| [die()](https://www.runoob.com/jquery/event-die.html)        | 在版本 1.9 中被移除。移除所有通过 live() 方法添加的事件处理程序 |
| [error()](https://www.runoob.com/jquery/event-error.html)    | 在版本 1.8 中被废弃。添加/触发 error 事件                    |
| [event.currentTarget](https://www.runoob.com/jquery/jq-event-currenttarget.html) | 在事件冒泡阶段内的当前 DOM 元素                              |
| [event.data](https://www.runoob.com/jquery/event-data.html)  | 包含当前执行的处理程序被绑定时传递到事件方法的可选数据       |
| [event.delegateTarget](https://www.runoob.com/jquery/event-delegatetarget.html) | 返回当前调用的 jQuery 事件处理程序所添加的元素               |
| [event.isDefaultPrevented()](https://www.runoob.com/jquery/event-isdefaultprevented.html) | 返回指定的 event 对象上是否调用了 event.preventDefault()     |
| [event.isImmediatePropagationStopped()](https://www.runoob.com/jquery/event-isimmediatepropagationstopped.html) | 返回指定的 event 对象上是否调用了 event.stopImmediatePropagation() |
| [event.isPropagationStopped()](https://www.runoob.com/jquery/event-ispropagationstopped.html) | 返回指定的 event 对象上是否调用了 event.stopPropagation()    |
| [event.namespace](https://www.runoob.com/jquery/event-namespace.html) | 返回当事件被触发时指定的命名空间                             |
| [event.pageX](https://www.runoob.com/jquery/event-pagex.html) | 返回相对于文档左边缘的鼠标位置                               |
| [event.pageY](https://www.runoob.com/jquery/event-pagey.html) | 返回相对于文档上边缘的鼠标位置                               |
| [event.preventDefault()](https://www.runoob.com/jquery/event-preventdefault.html) | 阻止事件的默认行为                                           |
| [event.relatedTarget](https://www.runoob.com/jquery/jq-event-relatedtarget.html) | 返回当鼠标移动时哪个元素进入或退出                           |
| [event.result](https://www.runoob.com/jquery/event-result.html) | 包含由被指定事件触发的事件处理程序返回的最后一个值           |
| [event.stopImmediatePropagation()](https://www.runoob.com/jquery/event-stopimmediatepropagation.html) | 阻止其他事件处理程序被调用                                   |
| [event.stopPropagation()](https://www.runoob.com/jquery/event-stoppropagation.html) | 阻止事件向上冒泡到 DOM 树，阻止任何父处理程序被事件通知      |
| [event.target](https://www.runoob.com/jquery/jq-event-target.html) | 返回哪个 DOM 元素触发事件                                    |
| [event.timeStamp](https://www.runoob.com/jquery/jq-event-timestamp.html) | 返回从 1970 年 1 月 1 日到事件被触发时的毫秒数               |
| [event.type](https://www.runoob.com/jquery/jq-event-type.html) | 返回哪种事件类型被触发                                       |
| [event.which](https://www.runoob.com/jquery/event-which.html) | 返回指定事件上哪个键盘键或鼠标按钮被按下                     |
| [event.metaKey](https://www.runoob.com/jquery/event_metakey.html) | 事件触发时 META 键是否被按下                                 |
| [focus()](https://www.runoob.com/jquery/event-focus.html)    | 添加/触发 focus 事件                                         |
| [focusin()](https://www.runoob.com/jquery/event-focusin.html) | 添加事件处理程序到 focusin 事件                              |
| [focusout()](https://www.runoob.com/jquery/event-focusout.html) | 添加事件处理程序到 focusout 事件                             |
| [hover()](https://www.runoob.com/jquery/event-hover.html)    | 添加两个事件处理程序到 hover 事件                            |
| [keydown()](https://www.runoob.com/jquery/event-keydown.html) | 添加/触发 keydown 事件                                       |
| [keypress()](https://www.runoob.com/jquery/event-keypress.html) | 添加/触发 keypress 事件                                      |
| [keyup()](https://www.runoob.com/jquery/event-keyup.html)    | 添加/触发 keyup 事件                                         |
| [live()](https://www.runoob.com/jquery/event-live.html)      | 在版本 1.9 中被移除。添加一个或多个事件处理程序到当前或未来的被选元素 |
| [load()](https://www.runoob.com/jquery/event-load.html)      | 在版本 1.8 中被废弃。添加一个事件处理程序到 load 事件        |
| [mousedown()](https://www.runoob.com/jquery/event-mousedown.html) | 添加/触发 mousedown 事件                                     |
| [mouseenter()](https://www.runoob.com/jquery/event-mouseenter.html) | 添加/触发 mouseenter 事件                                    |
| [mouseleave()](https://www.runoob.com/jquery/event-mouseleave.html) | 添加/触发 mouseleave 事件                                    |
| [mousemove()](https://www.runoob.com/jquery/event-mousemove.html) | 添加/触发 mousemove 事件                                     |
| [mouseout()](https://www.runoob.com/jquery/event-mouseout.html) | 添加/触发 mouseout 事件                                      |
| [mouseover()](https://www.runoob.com/jquery/event-mouseover.html) | 添加/触发 mouseover 事件                                     |
| [mouseup()](https://www.runoob.com/jquery/event-mouseup.html) | 添加/触发 mouseup 事件                                       |
| [off()](https://www.runoob.com/jquery/event-off.html)        | 移除通过 on() 方法添加的事件处理程序                         |
| [on()](https://www.runoob.com/jquery/event-on.html)          | 向元素添加事件处理程序                                       |
| [one()](https://www.runoob.com/jquery/event-one.html)        | 向被选元素添加一个或多个事件处理程序。该处理程序只能被每个元素触发一次 |
| [$.proxy()](https://www.runoob.com/jquery/event-proxy.html)  | 接受一个已有的函数，并返回一个带特定上下文的新的函数         |
| [ready()](https://www.runoob.com/jquery/event-ready.html)    | 规定当 DOM 完全加载时要执行的函数                            |
| [resize()](https://www.runoob.com/jquery/event-resize.html)  | 添加/触发 resize 事件                                        |
| [scroll()](https://www.runoob.com/jquery/event-scroll.html)  | 添加/触发 scroll 事件                                        |
| [select()](https://www.runoob.com/jquery/event-select.html)  | 添加/触发 select 事件                                        |
| [submit()](https://www.runoob.com/jquery/event-submit.html)  | 添加/触发 submit 事件                                        |
| [toggle()](https://www.runoob.com/jquery/event-toggle.html)  | 在版本 1.9 中被移除。添加 click 事件之间要切换的两个或多个函数 |
| [trigger()](https://www.runoob.com/jquery/event-trigger.html) | 触发绑定到被选元素的所有事件                                 |
| [triggerHandler()](https://www.runoob.com/jquery/event-triggerhandler.html) | 触发绑定到被选元素的指定事件上的所有函数                     |
| [unbind()](https://www.runoob.com/jquery/event-unbind.html)  | 从被选元素上移除添加的事件处理程序                           |
| [undelegate()](https://www.runoob.com/jquery/event-undelegate.html) | 从现在或未来的被选元素上移除事件处理程序                     |
| [unload()](https://www.runoob.com/jquery/event-unload.html)  | 在版本 1.8 中被废弃。添加事件处理程序到 unload 事件          |
| [contextmenu()](https://www.runoob.com/jquery/event-contextmenu.html) | 添加事件处理程序到 contextmenu 事件                          |
| [$.holdReady()](https://www.runoob.com/jquery/event-holdready.html) | 用于暂停或恢复.ready() 事件的执行                            |

##### jQuery动画效果：

### 语法:

``` js

//隐藏与显示
$(selector).hide(speed,callback)

//隐藏代码 后面跟的事件速度 回调函数
$(selector).show(speed,callback)

//显示代码     后面隔得时间速度    回调函数
toggle()   //也可以切换其他属性

//通过 jQuery，您可以使用 toggle() 方法来切换 hide() 和 show() 方法。
//显示被隐藏的元素，并隐藏已显示的元素：

```

### jQuery 动画效果 参考手册：

| 方法                                                         | 描述                                         |
| :----------------------------------------------------------- | :------------------------------------------- |
| [animate()](https://www.runoob.com/jquery/eff-animate.html)  | 对被选元素应用"自定义"的动画                 |
| [clearQueue()](https://www.runoob.com/jquery/eff-clearqueue.html) | 对被选元素移除所有排队函数（仍未运行的）     |
| [delay()](https://www.runoob.com/jquery/eff-delay.html)      | 对被选元素的所有排队函数（仍未运行）设置延迟 |
| [dequeue()](https://www.runoob.com/jquery/eff-dequeue.html)  | 移除下一个排队函数，然后执行函数             |
| [fadeIn()](https://www.runoob.com/jquery/eff-fadein.html)    | 逐渐改变被选元素的不透明度，从隐藏到可见     |
| [fadeOut()](https://www.runoob.com/jquery/eff-fadeout.html)  | 逐渐改变被选元素的不透明度，从可见到隐藏     |
| [fadeTo()](https://www.runoob.com/jquery/eff-fadeto.html)    | 把被选元素逐渐改变至给定的不透明度           |
| [fadeToggle()](https://www.runoob.com/jquery/eff-fadetoggle.html) | 在 fadeIn() 和 fadeOut() 方法之间进行切换    |
| [finish()](https://www.runoob.com/jquery/eff-finish.html)    | 对被选元素停止、移除并完成所有排队动画       |
| [hide()](https://www.runoob.com/jquery/eff-hide.html)        | 隐藏被选元素                                 |
| [queue()](https://www.runoob.com/jquery/eff-queue.html)      | 显示被选元素的排队函数                       |
| [show()](https://www.runoob.com/jquery/eff-show.html)        | 显示被选元素                                 |
| [slideDown()](https://www.runoob.com/jquery/eff-slidedown.html) | 通过调整高度来滑动显示被选元素               |
| [slideToggle()](https://www.runoob.com/jquery/eff-slidetoggle.html) | slideUp() 和 slideDown() 方法之间的切换      |
| [slideUp()](https://www.runoob.com/jquery/eff-slideup.html)  | 通过调整高度来滑动隐藏被选元素               |
| [stop()](https://www.runoob.com/jquery/eff-stop.html)        | 停止被选元素上当前正在运行的动画             |
| [toggle()](https://www.runoob.com/jquery/eff-toggle.html)    | hide() 和 show() 方法之间的切换              |

### jQuery选择器：

通过 $(":button") 可以选取所有 type="button" 的 <input> 元素 和

<button> 元素，如果去掉冒号，$("button")只能获取 <button> 元素。

关于 : 和 [ ] 这两个符号的理解

：可以理解为种类的意思，如：p:first，p 的种类为第一个。

[ ] 很自然的可以理解为属性的意思，如：[href] 选取带有 href 属性的元素。

###   jQuery 选择器 参考手册：

| 选择器                                                       | 实例                          | 选取                                                         |
| :----------------------------------------------------------- | :---------------------------- | :----------------------------------------------------------- |
| [*](https://www.runoob.com/jquery/jq-sel-all.html)           | $("*")                        | 所有元素                                                     |
| [#*id*](https://www.runoob.com/jquery/jq-sel-id.html)        | $("#lastname")                | id="lastname" 的元素                                         |
| [.*class*](https://www.runoob.com/jquery/jq-sel-class.html)  | $(".intro")                   | class="intro" 的所有元素                                     |
| [.*class,*.*class*](https://www.runoob.com/jquery/sel-multiple-classes.html) | $(".intro,.demo")             | class 为 "intro" 或 "demo" 的所有元素                        |
| [*element*](https://www.runoob.com/jquery/jq-sel-element.html) | $("p")                        | 所有 <p> 元素                                                |
| [*el1*,*el2*,*el3*](https://www.runoob.com/jquery/sel-multiple-elements.html) | $("h1,div,p")                 | 所有 <h1>、<div> 和 <p> 元素                                 |
| [:first](https://www.runoob.com/jquery/sel-first.html)       | $("p:first")                  | 第一个 <p> 元素                                              |
| [:last](https://www.runoob.com/jquery/sel-last.html)         | $("p:last")                   | 最后一个 <p> 元素                                            |
| [:even](https://www.runoob.com/jquery/sel-even.html)         | $("tr:even")                  | 所有偶数 <tr> 元素，索引值从 0 开始，第一个元素是偶数 (0)，第二个元素是奇数 (1)，以此类推。 |
| [:odd](https://www.runoob.com/jquery/sel-odd.html)           | $("tr:odd")                   | 所有奇数 <tr> 元素，索引值从 0 开始，第一个元素是偶数 (0)，第二个元素是奇数 (1)，以此类推。 |
| [:first-child](https://www.runoob.com/jquery/jq-sel-firstchild.html) | $("p:first-child")            | 属于其父元素的第一个子元素的所有 <p> 元素                    |
| [:first-of-type](https://www.runoob.com/jquery/sel-firstoftype.html) | $("p:first-of-type")          | 属于其父元素的第一个 <p> 元素的所有 <p> 元素                 |
| [:last-child](https://www.runoob.com/jquery/sel-lastchild.html) | $("p:last-child")             | 属于其父元素的最后一个子元素的所有 <p> 元素                  |
| [:last-of-type](https://www.runoob.com/jquery/sel-lastoftype.html) | $("p:last-of-type")           | 属于其父元素的最后一个 <p> 元素的所有 <p> 元素               |
| [:nth-child(*n*)](https://www.runoob.com/jquery/sel-nthchild.html) | $("p:nth-child(2)")           | 属于其父元素的第二个子元素的所有 <p> 元素                    |
| [:nth-last-child(*n*)](https://www.runoob.com/jquery/sel-nthlastchild.html) | $("p:nth-last-child(2)")      | 属于其父元素的第二个子元素的所有 <p> 元素，从最后一个子元素开始计数 |
| [:nth-of-type(*n*)](https://www.runoob.com/jquery/sel-nthoftype.html) | $("p:nth-of-type(2)")         | 属于其父元素的第二个 <p> 元素的所有 <p> 元素                 |
| [:nth-last-of-type(*n*)](https://www.runoob.com/jquery/sel-nthlastoftype.html) | $("p:nth-last-of-type(2)")    | 属于其父元素的第二个 <p> 元素的所有 <p> 元素，从最后一个子元素开始计数 |
| [:only-child](https://www.runoob.com/jquery/sel-onlychild.html) | $("p:only-child")             | 属于其父元素的唯一子元素的所有 <p> 元素                      |
| [:only-of-type](https://www.runoob.com/jquery/sel-onlyoftype.html) | $("p:only-of-type")           | 属于其父元素的特定类型的唯一子元素的所有 <p> 元素            |
| [parent > child](https://www.runoob.com/jquery/sel-parent-child.html) | $("div > p")                  | <div> 元素的直接子元素的所有 <p> 元素                        |
| [parent descendant](https://www.runoob.com/jquery/sel-parent-descendant.html) | $("div p")                    | <div> 元素的后代的所有 <p> 元素                              |
| [element + next](https://www.runoob.com/jquery/sel-previous-next.html) | $("div + p")                  | 每个 <div> 元素相邻的下一个 <p> 元素                         |
| [element ~ siblings](https://www.runoob.com/jquery/sel-previous-siblings.html) | $("div ~ p")                  | <div> 元素同级的所有 <p> 元素                                |
| [:eq(*index*)](https://www.runoob.com/jquery/sel-eq.html)    | $("ul li:eq(3)")              | 列表中的第四个元素（index 值从 0 开始）                      |
| [:gt(*no*)](https://www.runoob.com/jquery/sel-gt.html)       | $("ul li:gt(3)")              | 列举 index 大于 3 的元素                                     |
| [:lt(*no*)](https://www.runoob.com/jquery/sel-lt.html)       | $("ul li:lt(3)")              | 列举 index 小于 3 的元素                                     |
| [:not(*selector*)](https://www.runoob.com/jquery/jq-sel-not.html) | $("input:not(:empty)")        | 所有不为空的输入元素                                         |
| [:header](https://www.runoob.com/jquery/sel-header.html)     | $(":header")                  | 所有标题元素 <h1>, <h2> ...                                  |
| [:animated](https://www.runoob.com/jquery/sel-animated.html) | $(":animated")                | 所有动画元素                                                 |
| [:focus](https://www.runoob.com/jquery/jq-sel-focus.html)    | $(":focus")                   | 当前具有焦点的元素                                           |
| [:contains(*text*)](https://www.runoob.com/jquery/sel-contains.html) | $(":contains('Hello')")       | 所有包含文本 "Hello" 的元素                                  |
| [:has(*selector*)](https://www.runoob.com/jquery/sel-has.html) | $("div:has(p)")               | 所有包含有 <p> 元素在其内的 <div> 元素                       |
| [:empty](https://www.runoob.com/jquery/jq-sel-empty.html)    | $(":empty")                   | 所有空元素                                                   |
| [:parent](https://www.runoob.com/jquery/sel-parent.html)     | $(":parent")                  | 匹配所有含有子元素或者文本的父元素。                         |
| [:hidden](https://www.runoob.com/jquery/sel-hidden.html)     | $("p:hidden")                 | 所有隐藏的 <p> 元素                                          |
| [:visible](https://www.runoob.com/jquery/sel-visible.html)   | $("table:visible")            | 所有可见的表格                                               |
| [:root](https://www.runoob.com/jquery/jq-sel-root.html)      | $(":root")                    | 文档的根元素                                                 |
| [:lang(*language*)](https://www.runoob.com/jquery/jq-sel-lang.html) | $("p:lang(de)")               | 所有 lang 属性值为 "de" 的 <p> 元素                          |
| [[*attribute*\]](https://www.runoob.com/jquery/jq-sel-attribute.html) | $("[href]")                   | 所有带有 href 属性的元素                                     |
| [[*attribute*=*value*\]](https://www.runoob.com/jquery/sel-attribute-equal-value.html) | $("[href='default.htm']")     | 所有带有 href 属性且值等于 "default.htm" 的元素              |
| [[*attribute*!=*value*\]](https://www.runoob.com/jquery/sel-attribute-notequal-value.html) | $("[href!='default.htm']")    | 所有带有 href 属性且值不等于 "default.htm" 的元素            |
| [[*attribute*$=*value*\]](https://www.runoob.com/jquery/sel-attribute-end-value.html) | $("[href$='.jpg']")           | 所有带有 href 属性且值以 ".jpg" 结尾的元素                   |
| [[*attribute*\|=*value*\]](https://www.runoob.com/jquery/sel-attribute-prefix-value.html) | $("[title\|='Tomorrow']")     | 所有带有 title 属性且值等于 'Tomorrow' 或者以 'Tomorrow' 后跟连接符作为开头的字符串 |
| [[*attribute*^=*value*\]](https://www.runoob.com/jquery/sel-attribute-beginning-value.html) | $("[title^='Tom']")           | 所有带有 title 属性且值以 "Tom" 开头的元素                   |
| [[*attribute*~=*value*\]](https://www.runoob.com/jquery/sel-attribute-contains-value.html) | $("[title~='hello']")         | 所有带有 title 属性且值包含单词 "hello" 的元素               |
| [[*attribute**=*value*\]](https://www.runoob.com/jquery/sel-attribute-contains-string-value.html) | $("[title*='hello']")         | 所有带有 title 属性且值包含字符串 "hello" 的元素             |
| [[*name*=*value*\][*name2*=*value2*]](https://www.runoob.com/jquery/sel-multipleattribute-equal-value.html) | $( "input[id][name$='man']" ) | 带有 id 属性，并且 name 属性以 man 结尾的输入框              |
| [:input](https://www.runoob.com/jquery/sel-input.html)       | $(":input")                   | 所有 input 元素                                              |
| [:text](https://www.runoob.com/jquery/sel-input-text.html)   | $(":text")                    | 所有带有 type="text" 的 input 元素                           |
| [:password](https://www.runoob.com/jquery/sel-input-password.html) | $(":password")                | 所有带有 type="password" 的 input 元素                       |
| [:radio](https://www.runoob.com/jquery/sel-input-radio.html) | $(":radio")                   | 所有带有 type="radio" 的 input 元素                          |
| [:checkbox](https://www.runoob.com/jquery/sel-input-checkbox.html) | $(":checkbox")                | 所有带有 type="checkbox" 的 input 元素                       |
| [:submit](https://www.runoob.com/jquery/sel-input-submit.html) | $(":submit")                  | 所有带有 type="submit" 的 input 元素                         |
| [:reset](https://www.runoob.com/jquery/sel-input-reset.html) | $(":reset")                   | 所有带有 type="reset" 的 input 元素                          |
| [:button](https://www.runoob.com/jquery/sel-input-button.html) | $(":button")                  | 所有带有 type="button" 的 input 元素                         |
| [:image](https://www.runoob.com/jquery/sel-input-image.html) | $(":image")                   | 所有带有 type="image" 的 input 元素                          |
| [:file](https://www.runoob.com/jquery/sel-input-file.html)   | $(":file")                    | 所有带有 type="file" 的 input 元素                           |
| [:enabled](https://www.runoob.com/jquery/sel-input-enabled.html) | $(":enabled")                 | 所有启用的元素                                               |
| [:disabled](https://www.runoob.com/jquery/sel-input-disabled.html) | $(":disabled")                | 所有禁用的元素                                               |
| [:selected](https://www.runoob.com/jquery/sel-input-selected.html) | $(":selected")                | 所有选定的下拉列表元素                                       |
| [:checked](https://www.runoob.com/jquery/sel-input-checked.html) | $(":checked")                 | 所有选中的复选框选项                                         |
| .selector                                                    | $(selector).selector          | 在jQuery 1.7中已经不被赞成使用。返回传给jQuery()的原始选择器 |
| [:target](https://www.runoob.com/jquery/jq-sel-target.html)  | $( "p:target" )               | 选择器将选中ID和URI中一个格式化的标识符相匹配的<p>元素       |

### jQuery尺寸方法
``` js

$("button").click(function() {
    var txt = "";
    txt += "div 的宽度是: " + $("#div1").width() + "</br>";
    txt += "div 的高度是: " + $("#div1").height();
    $("#div1").html(txt);
})

```

## jQuery HTML / CSS 方法

下面的表格列出了所有用于处理 HTML 和 CSS 的 jQuery 方法。

下面的方法适用于 HTML 和 XML 文档。除了：html() 方法。

| 方法                                                         | 描述                                              |
| :----------------------------------------------------------- | :------------------------------------------------ |
| [addClass()](https://www.runoob.com/jquery/html-addclass.html) | 向被选元素添加一个或多个类名                      |
| [after()](https://www.runoob.com/jquery/html-after.html)     | 在被选元素后插入内容                              |
| [append()](https://www.runoob.com/jquery/html-append.html)   | 在被选元素的结尾插入内容                          |
| [appendTo()](https://www.runoob.com/jquery/html-appendto.html) | 在被选元素的结尾插入 HTML 元素                    |
| [attr()](https://www.runoob.com/jquery/html-attr.html)       | 设置或返回被选元素的属性/值                       |
| [before()](https://www.runoob.com/jquery/html-before.html)   | 在被选元素前插入内容                              |
| [clone()](https://www.runoob.com/jquery/html-clone.html)     | 生成被选元素的副本                                |
| [css()](https://www.runoob.com/jquery/css-css.html)          | 为被选元素设置或返回一个或多个样式属性            |
| [detach()](https://www.runoob.com/jquery/html-detach.html)   | 移除被选元素（保留数据和事件）                    |
| [empty()](https://www.runoob.com/jquery/html-empty.html)     | 从被选元素移除所有子节点和内容                    |
| [hasClass()](https://www.runoob.com/jquery/html-hasclass.html) | 检查被选元素是否包含指定的 class 名称             |
| [height()](https://www.runoob.com/jquery/css-height.html)    | 设置或返回被选元素的高度                          |
| [html()](https://www.runoob.com/jquery/html-html.html)       | 设置或返回被选元素的内容                          |
| [innerHeight()](https://www.runoob.com/jquery/html-innerheight.html) | 返回元素的高度（包含 padding，不包含 border）     |
| [innerWidth()](https://www.runoob.com/jquery/html-innerwidth.html) | 返回元素的宽度（包含 padding，不包含 border）     |
| [insertAfter()](https://www.runoob.com/jquery/html-insertafter.html) | 在被选元素后插入 HTML 元素                        |
| [insertBefore()](https://www.runoob.com/jquery/html-insertbefore.html) | 在被选元素前插入 HTML 元素                        |
| [offset()](https://www.runoob.com/jquery/css-offset.html)    | 设置或返回被选元素的偏移坐标（相对于文档）        |
| [offsetParent()](https://www.runoob.com/jquery/css-offsetparent.html) | 返回第一个定位的祖先元素                          |
| [outerHeight()](https://www.runoob.com/jquery/html-outerheight.html) | 返回元素的高度（包含 padding 和 border）          |
| [outerWidth()](https://www.runoob.com/jquery/html-outerwidth.html) | 返回元素的宽度（包含 padding 和 border）          |
| [position()](https://www.runoob.com/jquery/css-position.html) | 返回元素的位置（相对于父元素）                    |
| [prepend()](https://www.runoob.com/jquery/html-prepend.html) | 在被选元素的开头插入内容                          |
| [prependTo()](https://www.runoob.com/jquery/html-prependto.html) | 在被选元素的开头插入 HTML 元素                    |
| [prop()](https://www.runoob.com/jquery/html-prop.html)       | 设置或返回被选元素的属性/值                       |
| [remove()](https://www.runoob.com/jquery/html-remove.html)   | 移除被选元素（包含数据和事件）                    |
| [removeAttr()](https://www.runoob.com/jquery/html-removeattr.html) | 从被选元素移除一个或多个属性                      |
| [removeClass()](https://www.runoob.com/jquery/html-removeclass.html) | 从被选元素移除一个或多个类                        |
| [removeProp()](https://www.runoob.com/jquery/html-removeprop.html) | 移除通过 prop() 方法设置的属性                    |
| [replaceAll()](https://www.runoob.com/jquery/html-replaceall.html) | 把被选元素替换为新的 HTML 元素                    |
| [replaceWith()](https://www.runoob.com/jquery/html-replacewith.html) | 把被选元素替换为新的内容                          |
| [scrollLeft()](https://www.runoob.com/jquery/css-scrollleft.html) | 设置或返回被选元素的水平滚动条位置                |
| [scrollTop()](https://www.runoob.com/jquery/css-scrolltop.html) | 设置或返回被选元素的垂直滚动条位置                |
| [text()](https://www.runoob.com/jquery/html-text.html)       | 设置或返回被选元素的文本内容                      |
| [toggleClass()](https://www.runoob.com/jquery/html-toggleclass.html) | 在被选元素中添加/移除一个或多个类之间切换         |
| [unwrap()](https://www.runoob.com/jquery/html-unwrap.html)   | 移除被选元素的父元素                              |
| [val()](https://www.runoob.com/jquery/html-val.html)         | 设置或返回被选元素的属性值（针对表单元素）        |
| [width()](https://www.runoob.com/jquery/css-width.html)      | 设置或返回被选元素的宽度                          |
| [wrap()](https://www.runoob.com/jquery/html-wrap.html)       | 在每个被选元素的周围用 HTML 元素包裹起来          |
| [wrapAll()](https://www.runoob.com/jquery/html-wrapall.html) | 在所有被选元素的周围用 HTML 元素包裹起来          |
| [wrapInner()](https://www.runoob.com/jquery/html-wrapinner.html) | 在每个被选元素的内容周围用 HTML 元素包裹起来      |
| [$.escapeSelector()](https://www.runoob.com/jquery/html-escapeSelector.html) | 转义CSS选择器中有特殊意义的字符或字符串           |
| [$.cssHooks](https://www.runoob.com/jquery/html-csshooks.html) | 提供了一种方法通过定义函数来获取和设置特定的CSS值 |