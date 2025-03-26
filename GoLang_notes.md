# GoLang笔记

### 简介

Go是一个开源的编译型编程语言，由Google开发，于2009年首次公开发布。它语法简洁、干净且高效，

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

## Gorm

Golang出色的ORM（Object-Relational Mapping，对象关系映射）库，为Golang设计的ORM库，对开发者很友好。

#### 特性

- 全功能ORM
- 关联（Has One，Has Many，Belongs To，Many To Many，多态，单表继承）
- Create，Save，Update，Delete，Find 中钩子方法
- 支持 Preload、Joins 的预加载
- 事务，嵌套事务，Save Point，Rollback To Saved Point
- Context、预编译模式、DryRun模式
- 批量插入，FindInBatches、Fin/Create with Map，使用SQL表达式、Context Valuer 进行CRUD
- SQL构建起，Upsert，数据库锁，Optimizer/Index/Comment Hint，命名参数，子查询
- 复合主键，索引，约束
- Auto Migration
- 自定义Logger
- 灵活的可扩展插件API：Database Resolver（多数据库，读写分离）、Prometheus...
- 每个特性都经过了测试的重重考验
- 开发者友好

#### 安装

```sh
go get -u gorm.io/gorm
go get -u gorm.io/driver/sqlite
```

#### 简单示例

###### sqlite

```go
package main

import (
	"gorm.io/gorm"
    "gorm.io/driver/sqlite"
)

type Prodect struct {
    gorm.Model
    Code  string
    Price uint
}

func main() {
    db, err := gorm.Open(sqlite.Open("test.db"), &gorm.Config{})
    if err != nil {
        panic("failed to connect database")
    }
    
    // 迁移 schema
    db.AutoMigrate(&Product{})
    
    // Create
    db.Create(&Product{Code: "D42", Price: 100})
    
    // Read
    var product Product
    db.First(&product, 1)  // 根据整型主键查找
    db.First(&product, "code = ?", "D42")  // 查找 code 字段值为 D42 的记录
    
    // Update - 将 product 的 price 更新为 200
    db.Model(&product).Update("Price", 200)
    // Update - 更新多个字段
    db.Model(&product).Updates(Product{Price: 200, Code: "F42"})  // 仅仅更新非零值的字段
    db.Model(&product).Updates(map[string]interface{}{"Price": 200, "Code": "F42"})
    
    // Delete - 删除 product
    db.Delete(&product, 1)
}
```

###### mysql

```sh
# 安装
go get -u github.io/driver/mysql
```

示例

```go
package main

import (
	"github.com/gin-gonic/gin"
   	"gorm.io/gorm"
	"gorm.io/driver/mysql"
    "gorm.io/gorm/logger"
    "gorm.io/gorm/schema"
    "time"
    "github.com/shopspring/decimal"
)

func main() {
    dsn := "root:123456@tcp(127.0.0.1:3306)/company?charset=utf8mb4&parseTime=True&loc=Local"
	db, err := gorm.Open(mysql.Open(dsn), &gorm.Config{
        Logger: logger.Default.LogMode(logger.Info),  // 启用SQL日志，在控制台中输出SQL语句
        NamingStrategy: schema.NamingStrategy{
            SingularTable: true,  // 禁用复数表名（表明 = 结构提名 table 单数形式，不会出现 tables）
        }
    })
	if err != nil {
		panic("failed to connect database")
	}

	// 连接池
	sqlDB, err := db.DB()
	// SetMaxIdleConns 设置空闲连接池中连接的最大数量
	sqlDB.SetMaxIdleConns(10)
	// SetMaxOpenConns 设置打开数据库连接的最大数量
	sqlDB.SetMaxOpenConns(100)
	// SetConnMaxLifetime 设置了连接可复用的最大时间
	sqlDB.SetConnMaxLifetime(10 * time.Second)  // 10秒

	// 结构体
	type Staff struct {
        Id        int				`json:"id" gorm:"column:id;type:int(11);primaryKey;autoIncrement;comment:员工id"`
        Name      string			`json:"name" gorm:"column:name;type:varchar(30);comment:员工姓名"`
        Gender    string			`json:"gender" gorm:"column:gender;type:tinyint(1);comment:性别:1男 2女"`
        Work      string			`json:"work" gorm:"column:work;type:varchar(30);comment:员工职位"`
        Salary    decimal.Decimal	`json:"salary" gorm:"column:salary;type:decimal(10,2);comment:员工薪水"`
        DepId     int				`json:"depId" gorm:"column:dep_id;type:int(11);comment:部门id"`
        JoinTime  time.Time			`json:"joinTime" gorm:"column:join_time;type:datetime;default:current_timestamp;comment员工入职时间"`
        CreatedAt time.Time			`json:"createdAt" gorm:"column:created_at;type:datetime;default:current_timestamp;comment:创建时间"`
	}

	// 迁移
	db.AutoMigrate(&Staff{})
    
    // 设置路由
    router.GET("/list", func(c *gin.Context) {
		var dataList []Staff
		var total int64

		db.Model(dataList).Count(&total).Find(&dataList)
		c.JSON(200, gin.H{
            "code": 200,
			"data": dataList,
            "msg": "查询成功"
		})
	})
    
	router.Run("127.0.0.1:3000")
}
```

## 部署

### 1.打包到Linux

```sh
# 配置
set CGO_ENABLED=0
set GOOS=linux
set GOARCH=amd64

# 查看是否配置成功
go env

# 如果GOOS未配置成功
$env:GOOS="linux"

# 编译
go build -o app main.go
```

### 2.在服务器上运行

将打包好的程序上传到服务器

```sh
# 修改程序权限
chmod 777 app

# 运行
./app

# 后台运行
setsid ./app
```

### 3.映射域名

解析一个域名作为该服务接口地址

```sh
# 配置nginx
vim /etc/nginx/sites-available/api.example.com

# 配置文件内容
server {
    listen 80;
    server_name api.example.com;

    location / {
        proxy_pass http://localhost:8080;  # 替换为 Go 项目的监听端口（如 8080）
        proxy_set_header Host $host;
        proxy_set_header X-Real-IP $remote_addr;
        proxy_set_header X-Forwarded-For $proxy_add_x_forwarded_for;
        proxy_set_header X-Forwarded-Proto $scheme;
    }
}

# 启用配置
ls -s /etc/nginx/sites-available/api.example.com /etc/nginx/sites-enabled/
systemctl restart nginx

# 配置ssl证书
certbot --nginx -d api.example.com
```

