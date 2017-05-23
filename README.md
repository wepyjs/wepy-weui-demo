# WeUI in WePY

[WeUI](https://github.com/weui/weui-wxss) 是一套同微信原生视觉体验一致的基础样式库，由微信官方设计团队为微信内网页和微信小程序量身设计，令用户的使用感知更加统一。
这里是 WeUI 在 WePY 中的使用示例。

## 预览

[Web 版线上DEMO](https://www.madcoder.cn/demos/wepy-weui-demo/index.html)

![image](https://cloud.githubusercontent.com/assets/2182004/26298989/c0ae78b2-3f0b-11e7-8979-e37884a86a43.png)

## 体验步骤

### 1. 安装 wepy
本项目基于wepy开发，[参考这里](https://github.com/wepyjs/wepy)
```bash
npm install wepy-cli -g
```

### 2. 下载源代码
```bash
git clone git@github.com:wepyjs/wepy-weui-demo.git
```

### 3. 安装开发依赖
```bash
npm install
```

### 4. 编译源代码
```bash
wepy build
```

### 5.导入至开发者工具

编译完成后会生成`dist`目录，开发者工具本地开发目录指向`dist`目录。

**切记： 取消勾选`项目-->开启ES6转ES5`，否则代码运行报错。**

