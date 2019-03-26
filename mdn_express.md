# MDN教程：Express网页框架

> 
> MDN教程：[https://developer.mozilla.org/zh-CN/docs/Learn/Server-side/Express_Nodejs](https://developer.mozilla.org/zh-CN/docs/Learn/Server-side/Express_Nodejs)
> 
> MDN源码：[https://github.com/mdn/express-locallibrary-tutorial](https://github.com/mdn/express-locallibrary-tutorial)
> 
> GitHub：[https://github.com/mumingv/nodejs/tree/master/books/mdn-express](https://github.com/mumingv/nodejs/tree/master/books/mdn-express)

## 环境搭建

## 项目介绍

## 数据库

> 与数据库交互的两种方法：
> 
> 1、使用数据库的原生查询语言（如：SQL）；
> 
> 2、使用对象数据模型（ODM)或对象关系模型（ORM），ODM/ORM能够将数据表示为JavaScript对象，并将其映射到底层数据库。

**申请在线数据库**

在`mongodb`的官方网站[https://www.mongodb.com/](https://www.mongodb.com/)注册，并申请免费的数据库。

> 用户名：local_lib
> 
> 密码：Xu2iNONoZuC0DZ9H


**安装使用mongoose**

安装mongoose：

```
$ npm install mongoose
```

使用示例：

```
const mongoose = require('mongoose');
const mongoDB = 'mongodb+srv://local_lib:Xu2iNONoZuC0DZ9H@cluster-p0ynu.mongodb.net/test?retryWrites=true';
mongoose.connect(mongoDB);
mongoose.Promise = global.Promise;
const db = mongoose.connection;
db.on('error', console.error.bind(console, 'MongoDB 连接错误：'));
```

**导入测试数据**

```
$ npm install async
```
```
$ node populatedb.js 'mongodb+srv://local_lib:Xu2iNONoZuC0DZ9H@cluster-p0ynu.mongodb.net/test?retryWrites=true'
```

**创建模型文件**

创建目录`model`及其下面的目录文件。

```
model
├── author.js
├── book.js
├── bookinstance.js
└── genre.js
```

**本节代码**

[GitHub-Diff](https://github.com/mumingv/nodejs/commit/188b5cf743d91bca874ac23193af5e1d59733509)

## 路由和控制器

## 图书馆数据展示

## 表单

## 部署


