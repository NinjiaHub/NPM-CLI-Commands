# npm outdated

**检查过时的包**

### 梗概

```shell
$ npm outdated [[<@scope>/]<pkg> ...]
```

### 描述

该命令会查询注册表与当前已经安装的包做比对，看是否有过期的包。

输出结果：

* **wanted**：是指该包符合**package.json**文件中声明的符合 [SemVer](https://github.com/NinjiaHub/Tools-Tricks/blob/master/npm/documents/getting-started/SemVer.md) 范围的最大版本。如果没有可以使用的 SemVer 版本范围(例如使用 `npm outdated --global` 命令，或者该包在**package.json**文件中没有记录)，**wanted**这一列将会显示当前安装的版本号。
* **latest**：这一列中列出的是注册表中该包被打上**latest**标签的版本。使用**npm publish**命令时如果没有特殊的配置，则该包会被在发布时被打上**latest**的标签。**latest**标签标识的并不一定是该包的最大版本，也不一定是该包最近发布的版本，具体结果取决于开发者如何管理 **latest** [dist-tag](https://github.com/NinjiaHub/NPM-CLI-Commands/blob/master/documents/npm-dist-tag.md)。
* **location**：是指该包在依赖树中的层级位置。注意 **npm outdated** 命令默认使用**depth=0**，所以如果没有复写该选项，则只会输出过期的顶层依赖。
* **package type**(当使用--long／-l选项时)：显示一个包是**生产环境依赖(dependency)**还是**开发环境依赖(devDependency)**，**package.json**文件中没有记录的文件会被标识为**生产环境依赖**。

### 例子

```shell
$ npm outdated
Package      Current   Wanted   Latest  Location
glob          5.0.15   5.0.15    6.0.1  test-outdated-output
nothingness    0.0.3      git      git  test-outdated-output
npm            3.5.1    3.5.2    3.5.1  test-outdated-output
local-dev      0.0.3   linked   linked  test-outdated-output
once           1.3.2    1.3.3    1.3.3  test-outdated-output
```

**依赖(dependencies)**如下：

```package.json
{
  "glob": "^5.0.15",
  "nothingness": "github:othiym23/nothingness#master",
  "npm": "^3.5.1",
  "once": "^1.3.1"
}
```

* **glob** 的版本要求是 **^5**，所以npm不能安装 **glob@6**，因为 **glob@6** 不符合SemVer规定的版本范围。
* 使用Git指定的依赖每次都会重新安装。已经安装的[committish(commit-ish)](https://git-scm.com/docs/gitglossary#def_commit_object)可能符合依赖说明符(如果是一个不可变的符号，如提交对象的SHA)，也可能不符合，所以 `npm outdated` 和 `npm update` 需要从Git仓库拉取代码来检查。这也是为什么现在重新安装一个Git指定的依赖需要强制克隆然后安装的原因。
* **npm@3.5.2** 被标记为 **wanted**，但是 **latest** 却是指 **npm@3.5.1** 版本，这是因为npm使用 **dist-tags** 来管理 **latest** 和 **next** 发布通道。**npm update** 总是会安装最新版本，而 **npm install npm** 则会安装被打上 **latest** 标签的版本。
* **once** 只是单纯的过气了。重新安装 **node_modules** 或者运行 **npm update** 命令将会安装最新版本。

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

### See Also

* [npm-update](https://github.com/NinjiaHub/NPM-CLI-Commands/blob/master/documents/npm-update.md)
* [npm-dist-tag](https://github.com/NinjiaHub/NPM-CLI-Commands/blob/master/documents/npm-dist-tag.md)
* []()

## 原文链接

* [npm-uninstall](https://docs.npmjs.com/cli/outdated)

## 声明

本文翻译源内容来自网络，即NPM官方CLI文档，如有版权问题请联系译者。

侵删。

内容如有不恰当或错误，敬请指正。

译者邮箱：web.taox@gmail.com。

## Translator Info

* [GitHub](https://github.com/Tao-Quixote)
* Email: web.taox@gmail.com
