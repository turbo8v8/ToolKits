# NodeJS 相关的东西


官网下载编译好的包，解压，设置链接文件
``` shell
通过npm安装包：npm install [名称]@版本号 --save
下载安装依赖：npm install --production
移除包并修改记录文件：npm remove [名称] --save
```






## 自动构建工具

### Grunt

自动化配置工具——配置文件式写法

### gulp

自动化配置工具——Node调用API式写法，新的选它，喜欢这个模式和语法。

## Web 相关

### Express

- 官网： http://expressjs.com/

### KoaJS

- 官网： http://koajs.cn/

### React

- 网上一前端的评价，可参考：
那么，我从头开始创建 app 的首选方案是什么呢？
从长远而言，我个人倾向于选择 React，使用 Redux 架构，使用 Axios 支持 promise-ready 的 HTTP 请求，以及使用 react-router 处理路由。不过，这也取决于团队的经验：如果有专门写 HTML 和 CSS 的人，我肯定会选择 Angular。两个框架都各有利弊，从构建可维护项目的目的来考虑，最关键的还是如何让小伙伴们写出好代码。