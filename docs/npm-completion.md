# npm build

**实现 npm 命令的 tab 补全功能**

### 梗概

```shell
source <(npm completion)
```
### 描述

对所有npm命令开启 **tab 补全**功能。

上面**梗概**中介绍的方法是将补全功能引入当前的工作 shell 中。将 **npm completion** 的输出添加到 **~/.bashrc** 或者 ** ~/.zshrc** 中，将使补全功能可以在任意shell(包括新建的 shell 以及当前 shell 的子 shell)中使用：

```shell
npm completion >> ~/.bashrc
npm completion >> ~/.zshrc
```

如果你的系统在开机过程中会读取一个文件，例如 **/usr/local/etc/bash_completion.d/npm** 文件，那么你也可以通过 **管道** 或者 **重定向** 的方式将 **npm completion** 命令的输出结果保存在该文件中。

如果当前环境中定义了 **COMP_CWORD**, **COMP_LINE**, 以及 **COMP_POINT** 这几个环境变量，**npm completion** 命令将工作在 **管道模式(Plumbing mode)**，将基于给的参数输出 **补全相关的内容**。

### See Also

* [npm](https://github.com/NinjiaHub/NPM-CLI-Commands/blob/master/documents/npm.md"npm")

## 原文链接

* [npm-completion](https://docs.npmjs.com/cli/completion "npm-completion")

## 声明

本文翻译源内容来自网络，即NPM官方CLI文档，如有版权问题请联系译者。

侵删。

内容如有不恰当或错误，敬请指正。

译者邮箱：<web.taox@gmail.com>

## Translator Info

* [GitHub](https://github.com/Tao-Quixote)
* Email: <web.taox@gmail.com>