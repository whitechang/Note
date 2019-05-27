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
