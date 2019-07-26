# Node.JS 学习笔记

## Node基础
- Node.js是什么
  + JavaScript运行时，既不是语言，也不是框架，是一个平台
- Node.js中的JavaScript
  + 没有 BOM、DOM
  + EcmaSrcipt 基础JavaScript语言部分
  + 在Node中为JavaScript提供了一些服务器级别的API
    * 文件操作能力
    * http服务的能力
  + 模块系统
    * 在Node 中没有全局作用域的概念，只能通过require方法加载多个JavaScript脚本文件
    * 每个模块中，提供了`exports`对象，将要被外部访问的成员挂载到`exports`上面
  + 核心模块
    * Node提供的具名模块，如 fs文件操作模块、http网络服务模块、os操作系统模块、path路径处理模块
    * 所有模块需要使用`require`加载，如： `var fs = require('fs')`
  + 第三方模块
    * art-template node_modules
  + 自己写的模块
- 模块化 
  + 文件作用域
  + 通信规则
    * 加载require
    * 导出
- CommonJS 模块规范
  + 模块作用域
  + 使用require方法加载模块 ` var 自定义变量名 = require('模块') `
  + 使用exports 接口对象导出模块成员
    
## 服务的渲染
  - 服务端使用模板引擎，直接传页面到前端 （art-template）
  - 服务端渲染与客户端渲染的区别
    + 客户端渲染不利于SEO搜索引擎优化
    + 服务的渲染可以被爬虫抓取到

## 模块查找机制

+ 优先从缓存加载
+ 核心模块
+ 路径形式的文件模块
+ 第三方模块
  + node_modules/art-template/
  + node_modules/art-template/package.json
  + node_modules/art-template/package.json main
  + index.js 备选项
  + 如果没有node_modules 以此往上查找