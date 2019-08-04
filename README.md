# Webpack蛋炒饭
## 1、相关知识点


### 1.1、import(es6) 与 require(nodejs)

### 1.2、node中的path模块

#### 1.2.1 相对路径./问题
#### 1.2.2 魔法变量dirname的使用

### 1.3、正则表达式


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


