# npm ls

**列出已安装的npm包**

### 梗概

```shell
npm ls [[<@scope>/]<pkg> ...]

aliases: list, la, ll
```

### 描述

该命令会以树形结构列出所有已安装npm包及其依赖的版本，并输出到标准输出(即显示器)。

**位置参数** 是 **name@version-range** 这种标识符，这将会限制输出结果为匹配包名的那部分被输出，不匹配的则被忽略。注意，嵌套安装在npm包子目录中包，如果匹配**位置参数**，同样也会被显示输出。例如，运行 **npm ls npm -g**，输出结果如下：

```shell
/usr/local/lib
├── npm@5.5.1 
└─┬ nrm@1.0.2
  └── npm@3.10.10 
```

可以看到作为 **nrm** 依赖的 **npm@3.10.10** 也被列了出来。

该命令还会列出无关、缺失以及无效的包。

如果一个项目(npm包)使用 **git url** 来记录依赖，则会在 **name@version-range** 后的`()`中标识出来，以便于用户辨识这是一个项目的隐式fork。

显示的树形结构是基于包之间依赖关系的逻辑结构，而不是硬盘中 **node_modules** 目录中的物理结构。

当使用 **ll** 或者 **la** 时，默认显示扩展信息，如：

```shell
│ /usr/local/lib
│ 
├── gulp@3.9.1
│   The streaming build system
│   git+https://github.com/gulpjs/gulp.git
│   http://gulpjs.com
├── n@2.1.8
│   Interactively Manage All Your Node Versions
│   git://github.com/tj/n.git
│   https://github.com/tj/n
├── npm@5.5.1
│   a package manager for JavaScript
│   git+https://github.com/npm/npm.git
│   https://docs.npmjs.com/
...
```

### 配置

#### json

* 默认：false
* 类型：Boolean

以JSON格式显示信息

#### long

* 默认： false
* 类型： Boolean

显示完整信息

#### parseable

* 默认：false
* 类型：Boolean

显示可分析的输出，而不是树图

#### global

* 默认：false
* 类型：Boolean

检查全局安装前缀指定目录中的包，不检查当前项目中的包

#### depth

* 默认：0
* 类型：Int

设置要检查的依赖树的深度

#### prod / production

* 默认：false
* 类型：Boolean

是否只显示 **dependencies** 部分的依赖树

#### dev

* 默认：false
* 类型：Boolean

是否只显示 **devDependencies** 部分的依赖树

#### only

* 类型：String

当设置为 **dev** 或者 **development** 时，相当于 **dev**；

当设置为 **prod** 或者 **production** 时，相当于 **prod / production**

#### link

* 默认：false
* 类型：Boolean

只显示链接包(即通过 **npm link** 链接到指定位置的包)

### See Also


## 原文链接

* [npm-ls](https://docs.npmjs.com/cli/ls)

## 声明

本文翻译源内容来自网络，即NPM官方CLI文档，如有版权问题请联系译者。

侵删。

内容如有不恰当或错误，敬请指正。

译者邮箱：<web.taox@gmail.com>

## Translator Info

* [GitHub](https://github.com/Tao-Quixote)
* Email: <web.taox@gmail.com>
