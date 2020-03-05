# 4. 发布到Github

Github提供静态网页的托管服务，对于每个用户或组织，github都会为其分配一个`<UserName/OrgName>.github.io`的二级域名，这就很方便搭建项目主页。

搭建项目主页有以下几种方式：

- `master` 分支
- `master` 分支的 `/docs` 目录
- `gh-pages` 分支

可以用来搭建静态网站，比如静态blog、静态book等。

---

## 利用master分支

比较简单，自己摸索。

---

## 利用master分支中的docs目录

比较简单，自己摸索。

---

## 利用gh-pages部署

对于前两种，比较简单，笔者尝试了创建分支来建项目主页。

---

### 首次发布

在github上新建一个仓库取名为`LearnGitbook`，并用`README.md`初始化。

克隆到本地，创建新分支。

```git
git clone https://github.com/ACEKWA/LearnGitBook.git
cd LearnGitBook
git checkout -b gh-pages
```

当前clone下来的repo，保留`.git`，其余文件均删除。

把刚刚生成好的`_book`里面的文件复制到当前本地repo里。

```git
git add .
git commit -m "the first test to create a book"
git push -u origin gh-pages
```

笔者尝试的是向`organization`的`repository`进行`push`分支，第一次尝试没成功，第二次重新尝试才成功。第二次自动创建了一个私人许可。

---

### 书籍同步更新

如果书籍更新的怎么办呢？

还是在之前的`LearnGitBook`文件夹路径下打开`Git bash`，或者打开`Git Bash`进入此文件夹。如果之前没有切换到主分支的话，现在还是在`gh-pages`分支。如果不是想要的分支，可以用命令`git checkout gh-pages`切换到当前目标分支。

接下来就和之前的操作一样了，把当前文件夹的其他文件删除，保留`.git`，然后把新生成的书籍文件复制到当前文件夹，执行以下命令即可。

```git
git add .
git commit -m "update my book"
git push
```

---

### 参考博客

本书所写全部基于笔者经历经验，虽然搭建之前阅读了不少成功的博客案例，但是对有些命令的具体细微差别仍然不甚了解。

这里列出来几个博客，对于创建分支这一块儿参考了它们许多。

一来，作为对于本新人所写本文的补充；

二来，感谢他们写出了清晰的博文，希望能帮到更多的人。

1. [把gitbook发布在github](https://www.jianshu.com/p/e958df3381ad)
2. [结合 GitHub Pages 使用 GitBook](https://www.jianshu.com/p/3d03ab330df5)
3. [Github和GitBook使用](https://www.jianshu.com/p/925745669c6c) 详细的记录了github和gitbook的使用，其中包括创建干净的分支的方式。

---
