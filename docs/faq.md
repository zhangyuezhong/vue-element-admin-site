?> 提问之前，请先查阅下面的常见问题。

## vue-element-admin 和 vueAdmin-template 有什么区别？

vue-element-admin 是一个后台的集成方案，它囊括了很多的功能和组件，并不适合作为基础模板来进行二次开发。
vueAdmin-template 则是一个后台的基础模板脚手架，适合在它的基础上进行开发。

### 首先有任何报错，最简单的方法是报错信息复制到游览器里面搜索一下！
[google点我](http://lmgtfy.com/?q=%E6%90%9C%E4%B8%80%E6%90%9C)

[百度点我](http://www.baidu-x.com/?q=%E6%90%9C%E4%B8%80%E6%90%9C)

## vendor过大问题?
建议使用gzip，使用之后体积会只有原先1/3左右。还可以使用懒加载或者Code Splitting 建议参考[这篇文章](https://zhuanlan.zhihu.com/p/26710831)。打出来的 app.js 过大，查看一下是不是Uglify配置不正确或者sourceMap没弄对。
优化相关请看该[文章](https://zhuanlan.zhihu.com/p/27710902)


## 我的 url 里怎么有 # 号？要如何去掉？
请参考文档 [前端路由与服务端的结合](deploy.md?id=前端路由与服务端的结合) 主要由于 `browserHistory` 和 `hashHistory` 。


## npm install 总是失败？
由于中国墙的的原因，安装一些依赖时很容易出现超时问题，国内用户推荐使用淘宝源的安装方式
```bash
npm install --registry=https://registry.npm.taobao.org
```

## node-sass 安装失败？
[issues/25](https://github.com/PanJiaChen/vue-element-admin/issues/25)

[issues/24](https://github.com/PanJiaChen/vue-element-admin/issues/24)

## mock 问题
请参考文档 [Mock 和联调](mock-api) 主要由于 `browserHistory` 和 `hashHistory` 。


## 跨域问题 如：为什么发了一个 options  请求? Access-Control-Allow-Origin 报错等?
请参考文档 [跨域问题](cors.md)

## 图片 background url() 引用问题？
https://github.com/vuejs/vue-loader/issues/481

https://github.com/vuejs/vue-cli/issues/112

## can't not find 'xxModule' - 找不到某些依赖或者模块
这种情况一般报错信息可以看到是哪个包抛出的信息.
一般卸载这个模块,安装重新安装下即可.

## 我用了 axios , 为什么 IE 浏览器不识别(IE9+)
 IE 不支持 promise，所有需要单独引入 polyfill

 ```js
 npm install es6-promise

 // 在 main.js 引入即可
require("es6-promise").polyfill();
 ```

 ## 其它任何关于 vue 的问题 ？
 请你首先仔细阅读 vue [官方文档](https://cn.vuejs.org/index.html),但部分问题其实看报错就能知道了！


## 辅助文章
[Vue 脱坑记 - 查漏补缺(汇总下群里高频询问的xxx及给出不靠谱的解决方案)](https://juejin.im/post/59fa9257f265da43062a1b0e)
