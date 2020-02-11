# OI-best-articles

![](https://img.shields.io/badge/status-%F0%9F%95%8A-orange)

## 简介

如果你是一名 OI 选手，而且经常写博客/写 [OI Wiki](https://github.com/OI-Wiki/OI-Wiki)、看博客/看 [OI Wiki](https://oi-wiki.org) ，你可能早已发现，别人觉得通俗易懂的博客，在你看来可能缺乏严谨性；别人觉得细致入微的博客，在你看来可能觉得废话连篇。

实际上，无论一篇文章写得再好，它都不可能满足所有人的需求，而 OI-best-articles 正是想要打造一个 OI 相关文章的推荐平台，从严谨性、易懂性、详细程度等角度让用户对文章进行评价，并支持由用户提交文章链接。最后，用户可以根据多种指标对这些文章进行排序，找到令自己满意的一篇。

## 实现

由于动态站需要 $，而且自己建站的话难以保证同一个用户对同一篇文章只进行一次评价。所以选择使用 Github 的 issues 功能作为辅助，利用 Github API 实现评价的提交。
