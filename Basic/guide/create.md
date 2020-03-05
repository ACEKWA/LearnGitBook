# 3.1 新建

新建一个文件夹`LearnGitbook`作为第一本书。

进入此文件夹的路径，接下来的操作都在此文件夹路径下进行。

## 初始化

对于书籍进行初始化。

```shell
gitbook init
```

执行完之后，会发现文件夹中出现了`README.md`和`SUMMARY.md`两个文件。

- `README.md` 相当于封面或者前言。
- `SUMMARY.md` 是目录。

## 目录结构

初始化之后，`SUMMARY.md`中的内容如下。

```markdown
# Summary

* [Introduction](README.md)

```

如果写好了`SUMMARY.md`，然后用`init`进行初始化，那么`gitbook`会根据目录中的路径，自动创建好相应的文件。

列表加链接，链接中可以使用目录，也可以不必使用。

下边是本书的目录，暂且当作示例，之后可能会进行优化。看别人的目录并没有手动设置数字编号，但是我没设置的时候目录并没有自动编号，所以这里手动设置了一下，有空再看下这个地方怎么自动编号的。

```markdown
# Summary

* [前言](README.md)

## PART I - Gitbook Basic
* [1. 简要介绍](Basic/README.md)
* [2. 基本安装](Basic/install/README.md)
    - [2.1 安装Git](Basic/install/git.md)
    - [2.2 安装Node.js](Basic/install/nodejs.md)
    - [2.3 安装Gitbook](Basic/install/gitbook.md)
* [3. 基本使用](Basic/guide/README.md)
    + [3.1 新建](Basic/guide/create.md)
    + [3.2 编辑](Basic/guide/edit.md)
    + [3.3 输出](Basic/guide/build.md)
* [4. 发布到Github](Basic/release/README.md)

## Part II - Gitbook Advanced
* [1. 进阶概要](Advanced/README.md)
* [2. 插件](Advanced/plug-ins/README.md)
    * [2.1 暂时还没配置插件](Advanced/plug-ins/temp.md)
* [3. 自定义配置](Advanced/settings/README.md)
    + [3.1 book.json](Advanced/settings/bookjson.md)
    - [3.2 主题](Advanced/settings/theme.md)

## References
* [参考](references.md)

```
