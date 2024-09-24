# React笔记

### 简介

React 是一个用于构建用户界面的 JavaScript 库。

React 主要用于构建UI，很多人认为 React 就是 MVC 中的 V（视图view）。

React 起源于 FaceBook 的一个内部项目，用来架设 Instagram 的网站，并于 2013 年 5 月开源。

### React 特点

1. **声明式设计：** React 采用声明范式，可以轻松描述应用。
2. **高效：** React 通过对 DOM 模拟，最大限度的减少与 DOM 的交互。
3. **灵活：** React 可以与已知的库或框架更好的配合。
4. **JSX：** JSX 是 JavaScript 的语法拓展，React 开发并不一定使用 JSX，但一般都推荐使用 JSX。
5. **组件：** 通过 React 构建组件，使得代码更加容易得到复用，能够良好的应用在大项目的开发中。
6. **单向响应的数据流：** React 实现了单向响应的数据流，从而减少了重复代码，这也是它为什么比传统的数据绑定更简单。

### React 安装使用

#### 使用 Npm 创建

```sh

# 安装 create-react-app
npm install -g create-react-app

create-react-app <项目名称>


# npx 无需安装 create-react-app 创建项目
npx create-react-app

```

#### 使用 Next.js 框架创建

Next.js 的页面路由 **是一个全栈的 React 框架。** 它用途广泛，可让你创建任何规模的 React 应用程序——从大部分静态博客到复杂的动态的应用程序。

```sh
npx create-next-app
```

#### 使用 Remix 框架创建

Remix  **是一个具有嵌套路由的全栈式 React 框架。** 它可以把你的应用分成嵌套部分，该嵌套部分可以并行加载数据并响应用户操作进行刷新。

```sh
npx create-remix
```

