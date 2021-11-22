# Hello Word

## 计算机知识

##### 计算折扣价格

```apl
价格×(折扣÷10)=打折后价格
```

#####     也可以这样写：原价×0.折扣=打折后的价格；

#####     计算打几折

 价格÷打折后的价格=折扣；

## windows电脑快捷键：

```scss
ctrl + shift + t   // 重复上一步操作
```
## CMD命令：

 **win + r 输入cmd**

#### DOS命令
``` shell

dir  #查看计算机文件目录  /s 包括子目录 又称遍历目录

ping 192.168.1.1   #测试路由器
ping 127.0.0.1     #测试网卡
ping www.baidu.com #测试Internet

cd\ 切换c盘

# 查看已经连过的WiFi名
netsh
wlan show profiles 
# 查看选择WiFi名 的详细信息
wlan show profiles name="WiFi名" key=clear  


cd 目录名/目录           #进入目录
cd ..                   #返回上一级目录
rename 原文件名 新文件名 #重命名
dir                     #查看文件目录
E:                      #直接进入E盘
cls                     #清空命令
doskey /histry          #查看历史命令
color a                 #更改命令 字体背景颜色
md 目录名称              #创建目录
del 文件名               #删除文件

regedit   #注册表
calc      #计算器
cliconfg  #SQL SERVER 客户端网络实用程序
nodepad   #打开记事本
mstsc     #远程桌面连接
ctrl + c  #结束进程
```
## 计算机存储单位：

 计算机存储单位一般用bit、B、KB、MB、GB、TB、PB、EB、ZB、YB、BB、

 NB、DB......来表示，它们之间的关系是： 1024



![](https://gimg2.baidu.com/image_search/src=http%3A%2F%2Fwww.mianfeiwendang.com%2Fpic%2Fb38e795999720833623dca91%2F1-810-jpg_6-1080-0-0-1080.jpg)

## Git的使用：


 git init 初始化git生成git仓库

 git status 查看git状态

 git add filename添文件到暂存区

 git add .加入所有文件到暂存区

 git commite -m message提交文件到本地仓库

 git reset filename将尚没有commite之前加入到暂存区的文件重新

### 拉回

### 文件状态：

 1.没有被add过的文件叫untracked

 2.add之后文件处于staged状态等待commite

 3.commit之后文件处于unmodified这里之所以是modified是因为

 文件会跟仓库中的文件对比

 4.当unmodified的文件被修改则会变为modified状态

 5.modified之后的文件add之后将继续变为staged状态

 6.unmodifed的文件还有一种可能是已经不再需要了，那么可以

 remove它不再追踪变为untracked状态

## 转义字符：

**\ 转义字符**

| 转义字符 | 意义                                | ASCII码值（十进制） |
| -------- | ----------------------------------- | ------------------- |
| \a       | 响铃(BEL)                           | 007                 |
| \b       | 退格(BS) ，将当前位置移到前一列     | 008                 |
| \f       | 换页(FF)，将当前位置移到下页开头    | 012                 |
| \n       | 换行(LF) ，将当前位置移到下一行开头 | 010                 |
| \r       | 回车(CR) ，将当前位置移到本行开头   | 013                 |
| \t       | 水平制表(HT) （跳到下一个TAB位置）  | 009                 |
| \v       | 垂直制表(VT)                        | 011                 |
| \\       | 代表一个反斜线字符''\'              | 092                 |
| \'       | 代表一个单引号（撇号）字符          | 039                 |
| \"       | 代表一个双引号字符                  | 034                 |
| \?       | 代表一个问号                        | 063                 |
| \0       | 空字符(NUL)                         | 000                 |
| \ddd     | 1到3位八进制数所代表的任意字符      | 三位八进制          |
| \xhh     | 十六进制所代表的任意字符            | 十六进制            |



## Submile Text 实用快捷键：

```scss
ctrl + shift + p      //打开命令行窗口
ctrl + b              //运行程序
ctrl + enter          //建立 下一 空白行
ctrl + shift + [      //选中代码 折叠 ] 是展开
ctrl + shift + 上下键  //移动代码
```
## WebStorm 实用技巧&快捷键

```scss
alt + f12             //打开终端
ctrl + f12            //打开函数
ctrl + n              //打开类
ctrl + w              //会从小到大逐渐扩大。比如按一次,选中word，按两次，选择表达式, 三次,整个函数
shift + f6            //重构 重命名
f6                    //移动文件
ctrl + shift + 方向键  //移动代码
ctrl + d              //复制整行
ctrl + y              //删除整行
ctrl + ‐              //折叠光标所在的代码块
ctrl + +              //展开光标所在的代码块
ctrl + shift + ‐      //折叠全部代码块
ctrl + alt + ‐        //折叠代码块以及子代码块
ctrl + shift + l      //格式化代码
```
## Nvm ：nvm全名node.js version management，是一个node的版本管理工具。首先最重要的是：

一定要卸载已安装的 NodeJS，否则会发生冲突。然后下载 nvm-windows 最新安装包，直接安装即

可。

去GitHub上下载 [https://github.com/coreybutler/nvm‐windows/releases ](https://github.com/coreybutler/nvm‐windows/releases)

下载 nvm‐setup.zip



***Nvm 常用命令：***

```shell
#查看nvm版本
nvm version

#下载15.13.0版本的node
nvm install v15.13.0 

#卸载15.13.0版本的node
nvm uninstall v15.13.0

#查看已下载的node
nvm list 

#查看当前使用node的版本
nvm current 

#使用最新版本的node
nvm use node 

#查看网络可以安装的版本
nvm list available 

#打开node版本控制
nvm on 

#关闭node版本控制
nvm off 
```

## Typora 编辑器

***世界上最漂亮的写作APP   ——知乎***

Typora官网：[https://www.typora.io/](https://www.typora.io/)



Typora 常用的快捷键：

```scss
ctrl + k           //创建超链接
ctrl + /           //切换源码模式
ctrl + shift + i   //插入图片
ctrl + n           //打开新窗口 新建文件
```



