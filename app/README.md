# X-Sphere 前端部分

## 框架搭建

参考 [Taro 文档 4.x 版 - 安装及使用](https://taro-docs.jd.com/docs/next/GETTING-STARTED "https://taro-docs.jd.com/docs/4.x/GETTING-STARTED") 快速搭建基本框架。

1. 安装 `Taro CLI` 工具：

```Shell
# 查看版本
npm info @tarojs/cli

# 这里我们是用的是 4.x 版本，所以安装命令如下：
npm install -g @tarojs/cli@4.x

# 查看已安装版本
npm list -g @tarojs/cli
```

1. 创建模板项目：

```Shell
taro init app
👽 Taro v4.0.7



Taro 即将创建一个新项目!
Need help? Go and open issue: https://tls.jd.com/taro-issue-helper

? 请输入项目介绍 一系列小工具合集，以小程序形式存在
? 请选择框架 React
? 是否需要使用 TypeScript ？ Yes
? 请选择 CSS 预处理器（Sass/Less/Stylus） Sass
? 请选择包管理工具 yarn
? 请选择编译工具 Webpack5
? 请选择模板源 CLI 内置默认模板
⠦ 正在从 github:NervJS/taro-project-templates#v4.0 拉取远程模板...

# 执行失败，需要手动触发
cd app
yarn install
yarn install v1.22.22
info No lockfile found.
[1/4] Resolving packages...
...
[4/4] Building fresh packages...
success Saved lockfile.
Done in 32.72s.
```

1. 编译运行（编译成微信小程序）：

```Shell
# yarn
$ yarn dev:weapp
$ yarn build:weapp

# 仅限全局安装
$ taro build --type weapp --watch
$ taro build --type weapp

# npx 用户也可以使用
$ npx taro build --type weapp --watch
$ npx taro build --type weapp

# watch 同时开启压缩
$ set NODE_ENV=production && taro build --type weapp --watch # CMD
$ NODE_ENV=production taro build --type weapp --watch # Bash
```

1. 下载并打开[微信开发者工具](https://developers.weixin.qq.com/miniprogram/dev/devtools/download.html)，选择项目根目录以导入项目。

   - 需要设置关闭 ES6 转 ES5 功能，开启可能报错
   - 需要设置关闭上传代码时样式自动补全，开启可能报错
   - 需要设置关闭代码压缩上传，开启可能报错

### 注意事项

1. [常见问题](https://taro-docs.jd.com/docs/next/GETTING-STARTED#%E5%B8%B8%E8%A7%81%E9%97%AE%E9%A2%98)
