# Webpack
## 1、相关知识点


### 1.1、import(es6) 与 require(nodejs)
  require在node中的用法(加载并且运行module.export对象)

    1.路径形式的模块：require('./')

    2.核心模块的本质也是文件: require('http'), require('path')
    
    3.加载第三方模块：require('express')

    加载规则：既不是核心模块、也不是路径形式的模块
    先找到当前文件所处目录中的 node_modules 目录 -> 对应模块 -> package.json -> package.json 文件中的 main 属性(没有该属性就直接找该目录下index文件)

    import(es6)的模块系统（静态加载的）
    import命令会被 JavaScript 引擎静态分析，编译时加载模块
    require是运行时加载模块，只有运行时才知道,同步加载
    import()函数，完成动态加载、异步加载

### 1.2、node中的path模块

    path.resolve() 方法将路径或路径片段的序列解析为绝对路径。

    path.join() 方法使用平台特定的分隔符作为定界符将所有给定的 path 片段连接在一起，然后规范化生成的路径。

    _dirname变量获取当前模块文件所在目录的完整绝对路径(是一个全局变量)

    [参考node官网链接🔗](http://nodejs.cn/api/path.html#path_path_resolve_paths)


#### 1.2.1 相对路径./问题

  require中的相对路径./是不能省略的

### 1.3、正则表达式

  自行学习
  


## 2、webpack的基本配置参数

### 2.1、 entry: "./app/entry", // string | object | array

### 2.2、output: // webpack 如何输出结果的相关选项
   path: path.resolve(__dirname, "dist"), // string
    // 所有输出文件的目标路径
    // 必须是绝对路径（使用 Node.js 的 path 模块）

    filename: "bundle.js", // string    // 「入口分块(entry chunk)」的文件名模板

    publicPath: "/assets/", // string

### 2.3、module
  由于webpack本身只能解析js文件所以要借用各种loader的配置来处理.css .vue .mp4 .png等文件（这里结合一个loader栗子🌰说明）

### 2.3、resolve 解析

### 2.4、plugin 插件

### 2.5、devServer 运行时


## 3、vue-cli3 中的webpack配置


