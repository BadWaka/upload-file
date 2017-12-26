> GitHub 地址：https://github.com/BadWaka/upload-file

> 参考文章：[HTML上传文件的多种方式](https://www.jianshu.com/p/7636d5c60a8d)

# 实现上传文件（node 版本）

包括：
- 同步（h5表单）
- 异步（ajax）

## Get Start

前置条件：需要安装 node v4 版本以上

- clone 仓库代码
```
git clone https://github.com/BadWaka/upload-file.git
```

- 进入代码目录，安装所需依赖
```
cd upload-file
npm i
```

- 执行 node server.js，启动服务
```
node server.js
```

- 在浏览器打开 http://localhost:3000/sync.html 即可看到同步上传页面
![](http://upload-images.jianshu.io/upload_images/1828354-d3191fe39b6c057b.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

- 在浏览器打开 http://localhost:3000/async.html 即可看到异步上传页面
![](http://upload-images.jianshu.io/upload_images/1828354-a83074582d3c2f7e.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

- 选择文件后点击上传即可看到效果，在代码仓库的 uploads 目录下即可看到所上传的文件
![](http://upload-images.jianshu.io/upload_images/1828354-ab4e6e46a7d1ffb0.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

# 原理

## 服务端

服务端是使用 express 框架和库 multer 实现的文件上传功能

请求经过 multer 这个中间件，可以通过 req.files 或者 req.file 获得要上传的文件的信息，再通过 fs 模块写入到磁盘上

![](http://upload-images.jianshu.io/upload_images/1828354-648b7dc2b21aaa28.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

## 前端

### 同步原理

使用 h5 原生表单，form 配合 input[file]、input[submit]，指定接口（action），很轻松的实现
![](http://upload-images.jianshu.io/upload_images/1828354-335df7937c22e5d6.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

### 异步原理

- 监听 input[file] 元素的 onchange 事件，在选择文件完成后获取 fileList 文件列表对象
![](http://upload-images.jianshu.io/upload_images/1828354-5cb68cbaf5ee51f8.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

- 通过 ajax 和 formData 构建请求，请求后端接口
  - 可以通过 xhr.onload.onprogress 来获取上传的进度百分比
![](http://upload-images.jianshu.io/upload_images/1828354-84ef68b4a44d2727.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

# Thanks!
