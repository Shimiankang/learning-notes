# GoLang笔记

### 简介

Go是一个开源的编程语言，由Google开发，于2009年首次公开发布。它语法简洁、干净且高效

### 框架

- **Gin：** Gin是一个使用Go语言开发的Web框架。他提供类似Martin的API，但性能更加，速度提升高达40倍。

### 安装

直接前往官方下载地址下载 https://golang.google.cn/dl/

安装完后配置环境变量，例如：安装在C盘下就将 **C:\Go\bin** 添加到 **Path** 环境变量中，然后再创建工作目录 **C:\Go_WorkSpace**

检查是否安装成功

```sh
go version
```

启动Go

```sh
go run filename.go
```

编译Go

```sh
go build filename.go
```



## Gin框架

一个使用 Go 编写的 Web Framework 框架。

#### 特性

- **快速** 基于Radix树的路由，小内存占用。没有反射。可预测API性能。
- **支持中间件** 传入的HTTP请求可以由一系列中间件和最终操作来处理。例如：Logger、Authorization、GZIP，最终操作DB。
- **Crash处理** Gin可以catch一个发生在HTTP请求中的panic并recover它。这样，你的服务器将始终可用。例如：你可以向Sentry报告这个panic
- **JSON验证** Gin可以解析并验证请求的JSON，例如检查所需值的存在。
- **路由组** 更好的组织路由。是否需要授权，不同的API版本...此外，这些可以无限制嵌套而不会降低性能。
- **错误管理** Gin提供了一种方便的方法来收集HTTP请求期间发生的所有错误。最终，中间件可以将他们写入日志文件，数据库并通过网络发送。
- **内置渲染** Gin为JSON、XML和HTML渲染提供了易于使用的API。
- **可拓展性** 可以添加很多中间件，跟<a href="./JavaScript.md#Node.js">Node.js</a>一样

#### 简单示例

要求：电脑上已经安装Go1.16及以上版本

```sh
# 使用Go初始化一个项目
go mod init gin-demo	# 项目名称

# 安装Gin
go get -u github.com/gin-gonic/gin
#或
go install github.com/gin-gonic/gin@latest
```

创建 main.go 文件

```go
package main

import (
	"github.com/gin-gonic/gin"
)

func main() {
    router := gin.Default()
    router.GET("/", func(c *gin.Context) {
        c.JSON(200, gin.H{
            "msg": "Hello Gin Web Framework"
        })
    })
    router.Run()						// 默认端口8080
    // router.Run(":3000")				使用其他端口
    // router.Run("192.168.1.100:80")	绑定地址和端口
}
```

运行/启动

```sh
go run main.go
```

