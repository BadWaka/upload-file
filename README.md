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

# Thanks!
