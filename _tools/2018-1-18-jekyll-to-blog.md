---
type: tools
title: 使用jekyll搭建博客
---

[Jekyll on Windows | jekyll](https://jekyllrb.com/docs/windows/)
提供了windows下的Ubuntu实现，感觉很不错。可以试试。


- 写得很不错的：
[使用Github Pages建独立博客 | BeiYuu.com](http://beiyuu.com/github-pages)
[Jekyll搭建个人博客](http://baixin.io/2016/10/jekyll_tutorials1/)

写得很好的：
[Build your own website (with Jekyll and Minimal-mistakes theme) - Li Zeng](https://zenglix.github.io/personal_website/)

在这一步中，卡了好久：
- 设置：navigation.yml时，即设置不同的导航标签，类似这个：
关于navigation.yml中不同tab间的识别，还需要进一步学习。



### 其他
#### 数学公式 
- [Jekyll中使用MathJax](http://pkuwwt.github.io/linux/2013-12-03-jekyll-using-mathjax/)
不太起作用？

- [Kramdown does not seem to render math blocks · Issue #735 · mmistakes/minimal-mistakes](https://github.com/mmistakes/minimal-mistakes/issues/735)
mmistake作者解答：

在/_includes/scripts.html
中加入：
```
{% if page.mathjax %}
<script type="text/javascript" async
  src="https://cdn.mathjax.org/mathjax/latest/MathJax.js?config=TeX-MML-AM_CHTML">
</script>
{% endif %}

```

然后，在博客文章的yaml头部声明：
`mathjax: true`


## 多个导航栏
- [Github Pages博客搭建过程记录 @ 技术杂货铺hjmao](https://huajianmao.github.io/how-i-setup-this-blog/)