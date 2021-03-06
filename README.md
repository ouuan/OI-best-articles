# OI-best-articles

![](https://img.shields.io/badge/status-%F0%9F%95%8A-orange)

## 简介

如果你是一名 OI 选手，而且经常写博客/写 [OI Wiki](https://github.com/OI-Wiki/OI-Wiki)、看博客/看 [OI Wiki](https://oi-wiki.org) ，你可能早已发现，别人觉得通俗易懂的博客，在你看来可能缺乏严谨性；别人觉得细致入微的博客，在你看来可能觉得废话连篇。

实际上，无论一篇文章写得再好，它都不可能满足所有人的需求，而 OI-best-articles 正是想要打造一个 OI 相关文章的推荐平台，从严谨性、易懂性、详细程度等角度让用户对文章进行评价，并支持由用户提交文章链接。最后，用户可以根据多种指标对这些文章进行排序，找到令自己满意的一篇。

## 实现

由于动态站需要 $，而且自己建站的话难以保证同一个用户对同一篇文章只进行一次评价。所以选择使用 Github 的 issues 功能作为辅助，利用 Github API 实现评价的提交。

### 设想

1. 每个 topic 开一个 issue 用来存放标签下的文章，打上 label 用作标记。issue 内可以放这个 topic 的简介。
2. 支持自定义各项属性的权重加权排序。支持可选地隐藏各项属性均被另一篇文章完爆的文章。
3. 评价在本质上是发一条带有标题、链接、作者和评分的 issue comment，在网页上支持更加友好的 UI。
4. 新增文章等价于评价一篇本不存在的文章，在网页上支持更加友好的 UI。
5. 增加 topic 就是开 issue 并联系管理加 label。
6. topic 可以先参照 OI Wiki 目录并且预先把 OI Wiki 的链接加进来。
7. 属性：
   - 严谨性
   - 易懂性
   - 详细程度
   - 代码可读性
   - ……
8. 可以用 bot 账号发一条带有加密后 token 的 issue comment 来代替以用户身份发 issue comment，这样的话就可以在一个白嫖的伪动态站上实现同一用户单次评价 & 匿名评价，还可以少获取一些权限。
9. 易于设置（如，评分标准等），既便于更新维护，又可以方便地用于 OI 以外的领域。
10. 可以导出为静态站，定时同步到其它地方就能避免国内使用 GitHub API 遇到困难的情况。
