# npm edit

**编辑已安装的包**

### 梗概

```shell
npm edit <pkg>[@<version>]
```

### 描述

在系统默认编辑器(或者专门配置的 npm 编辑器 - 详情请戳[npm-config](https://NinjiaHub.github.io/NPM-CLI-Commands/docs/npm-config "npm-config"))中打开包目录。

在被编辑之后，该包会重新构建以便应用所有的更改。

例如，可以通过 **npm install connect** 命令安装 **connect** 包，然后运行 **npm edit connect** 对本地已安装拷贝的进行修改。

### 配置

#### editor

* 类型：path
* 默认：如果设置了 **EDITOR** 环境变量则使用该变量指定的值；否则，Posix系统 - **vi**，Windows系统 - **notepad**。

使用 **npm edit** 或者 **npm config edit** 命令时调用的编辑器。

### See Also

* [npm-explore](https://NinjiaHub.github.io/NPM-CLI-Commands/docs/npm-explore "npm-explore")
* [npm-install](https://NinjiaHub.github.io/NPM-CLI-Commands/docs/npm-install "npm-install")
* [npm-config](https://NinjiaHub.github.io/NPM-CLI-Commands/docs/npm-config "npm-config")

## 原文链接

* [npm-edit](https://docs.npmjs.com/cli/edit)

## 声明

本文翻译源内容来自网络，即NPM官方CLI文档，如有版权问题请联系译者。

侵删。

内容如有不恰当或错误，敬请指正。

译者邮箱：<web.taox@gmail.com>

## Translator Info

* [GitHub](https://github.com/Tao-Quixote)
* Email: <web.taox@gmail.com>
