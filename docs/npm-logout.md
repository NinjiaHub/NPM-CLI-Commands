# npm logout

**退出在当前配置中注册表中的登录**

### 梗概

```shell
npm logout [--registry=<url>] [--scope=<@scope>]
```

### 描述

如果登录的是一个支持基于 token 认证的注册表，则通知服务端结束该 token 的对话。该命令会使所有使用该 token 的环境失效，并不仅限于当前环境。

如果登录的是只支持用户名密码认证的注册表，则该操作会清空用户配置中的认证信息。在这种情况下，该命令的作用范围只限于当前环境。

如果使用了 **`--scope`** 选项，假如当前登录的注册表设置了域 (**scope**)，则该命令会找到当前注册表链接到已设置域 (**scope**)的认证信息并使之失效。

### 配置

#### registry

* 默认：[https://registry.npmjs.org/](https://registry.npmjs.org/)

npm包所在注册表的基本URL。如果没有设置 **scope** 则该配置优先。

#### scope

* 默认：当前项目的域(scope)

如果设置了该项，则退出指定的域的登录。详情请戳👉[npm scope](https://docs.npmjs.com/misc/scope)。

```shell
npm logout --scope=@myco
```

### See Also

* [npm-adduser](https://NinjiaHub.github.io/NPM-CLI-Commands/docs/npm-adduser "npm-adduser")
* [npm-config](https://NinjiaHub.github.io/NPM-CLI-Commands/docs/npm-config "npm-config")
* [npm-whoami](https://NinjiaHub.github.io/NPM-CLI-Commands/docs/npm-whoami "npm-whoami")

## 原文链接

* [npm-logout](https://docs.npmjs.com/cli/logout "npm logout")

## 声明

本文翻译源内容来自网络，即NPM官方CLI文档，如有版权问题请联系译者。

侵删。

内容如有不恰当或错误，敬请指正。

译者邮箱：<web.taox@gmail.com>

## Translator Info

* [GitHub](https://github.com/Tao-Quixote)
* Email: <web.taox@gmail.com>
