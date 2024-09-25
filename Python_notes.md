

# Python

#### 介绍

Python 是一门易于学习、功能强大的编程语言。它提供了高效的高级数据结构，还能简单有效的面向对象编程。

Python 优雅的语法和动态类型以及解释型语言的本质，使它成为多数平台上写脚本和快速开发应用的理想语言。

#### Python海龟制图

import  turtle   导入海归制图模块；

turtle.showturtle ( ) 显示箭头；turtle.write ("hello world") 书写字符串；turtle.forward( 像素 )  表示前进多少像素；

turtle.color( " color " )  更改画笔的颜色；turtle.left( 度数 )  向左旋转多少度；  turtle.goto( 0,0 )  去做表 (0,0)；

turtle.penup( ) 抬笔，路径不会画出来；turtle.pendown( ) 放笔，路径绘画出来；

turtle.circle( 100 )  画一个半径为100的圆；turtle.width( ) 设置画笔粗细；turtle.hideturtle( ) 隐藏箭头；



**Python一些内容：**

用 # 注释一行 ； 用 " " "    内容   " " "   注释多行；用 \ 连接行字符 只是把第二行的代码和第一行的代码链接一块形成一个完整的语句，不是说两个内容链接成一个内容；



**链式赋值：**x=y=123;   这样就把123赋给 x 和 y；相当于  x=123   y=123;

**系列解包赋值：**a,b,c=4,5,6  相当于：a=4 b=5 c=6;



**divmod**（被除数,除数）函数同时得到商和余数，返回一个元组；

**Python**中 int ( ) 整数型没有最大值限制想多大就多大没有long（）；float（）浮点型 

**Python**中逻辑运算符  逻辑或 or        逻辑且 and		   逻辑非   not

**Python** 中任何对象都能直接进行**真值测试**（测试该对象的布尔类型值为 True 或者 False），用于 if 或者 while 语句的条件判断，也可以做为布尔逻辑运算符的操作数。



**Python整数进制:**

Python中，除10进制，还有，其他三种进制：

·0b或0B，二进制 0  1

·0o或0O，八进制 0  1  2  3  4  5  6  7  

·0x或0X，十六进制 0 1 2 3 4 5 6 7 8 9 a b c d e f 

bin（） 二进制转换函数；oct（）八进制转换函数；int（）十进制转换也是整数型；

hex（）转换十六进制；



***字符串新函数：***

```python

#移除前缀字符代码： 
"祝您身体健康万事如意".removeprefix("祝")
#输出：
"您身体健康万事如意"

#移除后缀字符代码：
"祝您身体健康万事如意".removesuffix("意")
#输出：
"祝您身体健康万事如"

#过滤头尾字符串：
str = "123abcrunoob321" 
print (str.strip( '12' )) 

#切割：
split("_")

```

### Python中一些语法：

if __name__ == '__main__'的意思是：当.py文件被直接运行时，if __name__ == '__main__'之下的代码块将被运行；当.py文件以模块形式被导入时，if __name__ == '__main__'之下的代码块不被运行。



**Python 变量：**

``` python

#支持中文变量名
大大 = dada  #大大 的值为dada 

#支持多个变量赋值
a,b = 1,2  # a的值为1 b的值为2

#也可以赋值多个变量 
a = b = 3   #两个值都变成 3

```



**Python函数：**
``` python

#数组去除重复：
s=[1,1,1,2,2,3,3,4]
s2=list(set(s))
print(s2) #输出结果为[1,2,3,4]

range() #和循环一块使用
#函数原型：
range（start， end， scan):
#参数含义：start:计数从start开始。默认是从0开始。例如range（5）等价于range（0， 5）;
         # end:技术到end结束，但不包括end.例如：range（0， 5） 是[0, 1, 2, 3, 4]没有5
         # scan：每次跳跃的间距，默认为1。例如：range（0， 5） 等价于 range(0, 5, 1)

format() #字符串类型格式化输出
#代码：  
" { } ：您 { } 购买的 { } 到了" .format( "快递小哥","taobao","快递" )
#输出：
快递小哥：您taobao购买的快递到了

#代码：
" { 1 } ：您 { 2 } 购买的 { 0 } 到了" .format( "快递小哥","taobao","快递" )
#输出：
taobao：您快递购买的快递小哥到了

```



**Pycharm 快捷键：**

``` scss

Ctrl + Shift + L：//搜索
Ctrl + Alt + L：  //格式化代码
Ctrl + Shift + F：//高级查找

```


## Pychon模块

**python模块分为三类：内置模块、开源模块（第三方模块）、自定义模块**



当模块中没有类：	

**(1)如果使用import导入：import  test**

 调用方法：test.add(1)

**(2)使果用form...import导入：from  test import \***

 调用方法：add(1)



当模块中有类：类名为cal

**(1)如果使用import导入：import test**

 调用方法：test.cal().add(1)

**(2)如果使用from...import导入：from  test import \***

 调用方法：cal().add(1)



#### os模块
``` python

变量 = os.path.dirname( "/datou/wk/demo.py" )	   # 返回路径名
变量 = os.path.basename( "/datou/wk/demo.py" )   # 返回文件名
变量 = os.path.splitext( "/datou/wk/demo.py" )   # 分别返回文件名和路径名
os.path.exists("/dir") 							# 判断该目录是否存在 存在返回 true

```
#### threading模块（多线程）

``` python

#例如：
import time import threading 
start = time.perf_counter() 
def worker():   
    print("worker")
    time.sleep(1) 
    return 

if __name__ === "__main__":    
    for i in range(5): 
        t = threading.Thread(target=worker)     
        t.start()   
        end = time.perf_counter() 
        print(end-start)
        
```
#### IDM模块

#### Python with语句

有一些任务，可能事先需要设置，事后做清理工作。对于这种场景，Python的with语句提供了一种非常方便的处理方式。一个很好的例子是文件处理，你需要获取一个文件句柄，从文件中读取数据，然后关闭文件句柄。


``` python

#使用open语句读取文件： 
#普通读取可能处理异常 
file = open("./video/test.txt")
data = file.read() print(data)  

#使用with语句读取文件： 
#使用with语句读取可以有效避免异常 
with open("/tmp/foo.txt") as file:  
    data = file.read()
    
```
#### try、except、finally用法：

try, except, finally是Python中的异常捕捉机制，通常的用法就是try..except...结合起来用，程序捕捉try语句块中的异常，如果发现异常就把异常交给except中的语句块进行处理，也就是执行except中的语句，这里except也可以结合

``` python

#就像if else 的用法 
try:  
    print('hello') 
except:
    print('你好') 
finally:
    pass      # pass 通过的意思

```


#### open（）用法：
``` python

open(name[, mode[, buffering]]) 

# name : 一个包含了你要访问的文件名称的字符串值。 
# mode : mode 决定了打开文件的模式：只读，写入，追加等。所有可取值见如下的完全列表。这个参数是非强制的，默认文件访问模式为只读(r)。 
# buffering : 如果 buffering 的值被设为 0，就不会有寄存。如果 buffering 的值取 1，访问文件时会寄存行。如果将 buffering 的值设为大于 1 的整数，表明了这就是的寄存区的缓冲大小。如果取负值，寄存区的缓冲大小则为系统默认。

```

**mode 参数表：**

| 模式 | 描述                                                         |
| ---- | ------------------------------------------------------------ |
| t    | 文本模式 (默认)。                                            |
| x    | 写模式，新建一个文件，如果该文件已存在则会报错。             |
| b    | 二进制模式。                                                 |
| +    | 打开一个文件进行更新(可读可写)。                             |
| U    | 通用换行模式（不推荐）。                                     |
| r    | 以只读方式打开文件。文件的指针将会放在文件的开头。这是默认模式。 |
| rb   | 以二进制格式打开一个文件用于只读。文件指针将会放在文件的开头。这是默认模式。一般用于非文本文件如图片等。 |
| r+   | 打开一个文件用于读写。文件指针将会放在文件的开头。           |
| rb+  | 以二进制格式打开一个文件用于读写。文件指针将会放在文件的开头。一般用于非文本文件如图片等。 |
| w    | 打开一个文件只用于写入。如果该文件已存在则打开文件，并从开头开始编辑，即原有内容会被删除。如果该文件不存在，创建新文件。 |
| wb   | 以二进制格式打开一个文件只用于写入。如果该文件已存在则打开文件，并从开头开始编辑，即原有内容会被删除。如果该文件不存在，创建新文件。一般用于非文本文件如图片等。 |
| w+   | 打开一个文件用于读写。如果该文件已存在则打开文件，并从开头开始编辑，即原有内容会被删除。如果该文件不存在，创建新文件。 |
| wb+  | 以二进制格式打开一个文件用于读写。如果该文件已存在则打开文件，并从开头开始编辑，即原有内容会被删除。如果该文件不存在，创建新文件。一般用于非文本文件如图片等。 |
| a    | 打开一个文件用于追加。如果该文件已存在，文件指针将会放在文件的结尾。也就是说，新的内容将会被写入到已有内容之后。如果该文件不存在，创建新文件进行写入。 |
| ab   | 以二进制格式打开一个文件用于追加。如果该文件已存在，文件指针将会放在文件的结尾。也就是说，新的内容将会被写入到已有内容之后。如果该文件不存在，创建新文件进行写入。 |
| a+   | 打开一个文件用于读写。如果该文件已存在，文件指针将会放在文件的结尾。文件打开时会是追加模式。如果该文件不存在，创建新文件用于读写。 |
| ab+  | 以二进制格式打开一个文件用于追加。如果该文件已存在，文件指针将会放在文件的结尾。如果该文件不存在，创建新文件用于读写。 |

#### BeautifulSoup
``` python

from bs4 import BeautifulSoup 
text = BeautifulSoup(html)
print(text.select('a'))  #查看所有a标签   可以 #title 这样可以查看id为title的元素

```
#### Python3 BIF内置函数
``` python

#查看所有 内置函数 
dir(__builtins__) 

#转换成 整型数字
int()   

#转换成 浮点型数字
float() 

#返回一个复数，re 是实部 im 是虚部
complex(re,im)  

#返回绝对值
abs()  

```
#### 转义字符
``` python

print(r"D:\User\Dell")    # 输出结果  为  D:\User\Dell 
print("D:\\User\\Dell"")  # 输出结果  为  D:\User\Dell
      
```

#### Python 语句
``` python

a = "hello world" * 5             #赋值 5 个 hello world 给 a
a = """ 这个地方可以随便写文章 """   #长字符串  跨行字符串  Triple quoted 三引号字符串 
a = 3 // 2                        #地板出  确保两个数相处的结果为整数 如果不是整数 就向下取整

```
####  E记法

​	2e7，即：2 x10 x10 x10 x10 x10 x10 x10     

​	2e-7，即：0.0000002



**Python 中的 False：**

定义为 False 的对象：None 和 False 值为0的数字类型：0, 0.0, 0j, Decimal(0), Fraction(0.1) 空的序列和集合：'', (), [], {}, set(), range(0) 



**Python运算符优先级：**

  和JavaScript有点不一样

| 运算符说明 | Python运算符            | 优先级 | 结合性 | 优先级顺序 |
| ---------- | ----------------------- | ------ | ------ | :--------: |
| 小括号     | ( )                     | 19     | 无     |     高     |
| 索引运算符 | x[i] 或 x[i1: i2 [:i3]] | 18     | 左     |     ︿     |
| 属性访问   | x.attribute             | 17     | 左     |     \|     |
| 乘方       | **                      | 16     | 右     |     \|     |
| 按位取反   | ~                       | 15     | 右     |     \|     |
| 符号运算符 | +（正号）、-（负号）    | 14     | 右     |     \|     |
| 乘除       | *、/、//、%             | 13     | 左     |     \|     |
| 加减       | +、-                    | 12     | 左     |     \|     |
| 位移       | >>、<<                  | 11     | 左     |     \|     |
| 按位与     | &                       | 10     | 右     |     \|     |
| 按位异或   | ^                       | 9      | 左     |     \|     |
| 按位或     | \|                      | 8      | 左     |     \|     |
| 比较运算符 | ==、!=、>、>=、<、<=    | 7      | 左     |     \|     |
| is 运算符  | is、is not              | 6      | 左     |     \|     |
| in 运算符  | in、not in              | 5      | 左     |     \|     |
| 逻辑非     | not                     | 4      | 右     |     \|     |
| 逻辑与     | and                     | 3      | 左     |     \|     |
| 逻辑或     | or                      | 2      | 左     |     底     |
| 逗号运算符 | exp1, exp2              | 1      | 左     |            |

**分支语句(IF判断) | 循环语句**



### Pyinstaller 模块

**说明：**用来打包python文件的一个模块



**用法：**

```sh

#安装
pip install pyinstaller

#基础用法
pyinstaller -F 文件名.py

#设置icon
pyinstaller -F -i 图标.ico 文件名.py

```

**参数：**

| 参数                | 描述                               |
| ------------------- | ---------------------------------- |
| -h                  | 查看帮助                           |
| --clean             | 清理打包过程中的临时文件           |
| -D，--onedir        | 默认值，生成dist文件夹             |
| -F，--onefile       | 在dist文件夹中只生成独立的打包文件 |
| -i <图标文件名.ico> | 指定打包程序使用的图标（.ico）文件 |

python pywifi 暴力破解WiFi 文章地址；

http://t.csdn.cn/wGOzL