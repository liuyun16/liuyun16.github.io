---
type: tools
title: 使用Markdown写作并插入参考文献（atom+pandoc+Zotero）
date:  2018-2-24
---

## 1. 缘起
自从遇见Zotero，Markdown之后就再也不想用microsoft Word了，因为看见word的工具栏就想调格式有没有！！
加入到Markdown的阵营之后，格式全部交给了写完之后的css文件渲染，没有格式可调，觉得不写字出来就是逃避困难的表现。
但是，上周的一个学术写作却把自己给难住了，因为，我不会在markdown中插入文献！最后挣扎了几天，还是退回了word的阵营，感觉到了一点点的挫败。
因此，花费了一天的时间，我终于摸到了一些门道，争取在忘记之前写下来。

## 2. 实现逻辑
1. 利用文本编辑器(atom),使用Markdown输入内容；
2. 文献管理软件Zotero+插件[Better BibTeX for Zotero](https://retorque.re/zotero-better-bibtex/),管理文献并生成.bib的文献库索引；
3. Atom中安装插件[zotero-citations](https://atom.io/packages/zotero-citations)或者[zotero-picker](https://atom.io/packages/zotero-picker)，在markdown文本中插入Bibtexde citation key；
4. 利用pandoc 进行markdown的渲染以及转换，pandoc可以从.bib文件中根据citations key读取引文，生成参考文献格式，输出word文档或pdf。

## 3.具体步骤及解释
1. Better BibTeX for zotero是专门为LaTex引文管理与插入的插件，在zotero中安装之后，可以在每个item的`info`中，看到自动生成了`citations key`:

![img](https://farm5.staticflickr.com/4606/39569069925_76f6c32b69_o.png)

这个key唯一对应于一篇文献。

2. 通过导出，生成`library.bib`文件。
  - Zotero主菜单`File`-->`Export libray`-->`Format`勾选`Better BibLaTeX`，其他的Translator options可选；
![img](https://farm5.staticflickr.com/4759/40464977711_6ed5afc958_o.png)

 - 导出在特定的文件夹中，如`\MyProject\Library.bib`;
  用文本编辑器打开，会发现里面的内容为：

  ```
  @article{SanchezOXYGENVACANCYMODEL1987,
    title = {{{OXYGEN VACANCY MODEL IN STRONG METAL SUPPORT INTERACTION}}},
    volume = {104},
    issn = {0021-9517},
    doi = {10.1016/0021-9517(87)90342-3},
    shorttitle = {{{OXYGEN VACANCY MODEL IN STRONG METAL SUPPORT INTERACTION}}},
    number = {1},
    journaltitle = {Journal of Catalysis},
    date = {1987-03},
    pages = {120--135},
    author = {Sanchez, M. G. and Gazquez, J. L.},
    note = {00243}
  }
```

可以简单地理解为，`citations-key`为`SanchezOXYGENVACANCYMODEL1987`，其中对应了title，author以及期刊名称等信息。。最后生成的参考文献格式依赖于其中的内容。

3. 根据所投杂志要求，选取好自己所需要的参考文献格式，如选取`acs-nano`的引用格式，到网站（[Zotero Style Repository](https://www.zotero.org/styles)）上下载csl文件。
4. 将写作好的markdown文件此例为`input.md`与`library.bib`与`acs-nano.csl`文件放置于同一个文件夹中，
5. 下载并安装[Pandoc - Installing pandoc](http://pandoc.org/installing.html)。
6. 打开计算机终端或命令行，windows可以为`cmd.exe`或者`powershell.exe`,Linux为`bash`.
7. 运行`pandoc input.md --bibliography=library.bib --csl=acs-nano.csl -o output.docx`，

结果：你可以得到一个名为`output.docx`的文件。上述命令将 `input.md`转化成了`output.docx`。

通过这个方法，可以成功地实现.markdown 到.docx文件，.pdf（需要LaTex软件）等格式的文件了。
成功打通从markdown到其它格式文档的通道。


## 更多参考：
1. [Using Pandoc - YouTube](https://www.youtube.com/watch?v=N31E_NZYQQY&t=450s)，很好的pandoc转化markdown文件的教程；
2. [What's a bib file? - YouTube](https://www.youtube.com/watch?v=JF9bvYmcdmY)，介绍bib文件；
3. [Academic Markdown and Citations · Chris Krycho](http://www.chriskrycho.com/2015/academic-markdown-and-citations.html#fn1)，参考大概的转换文档的流程；
4. [My workflow for transforming academic Markdown into beautiful Word documents](http://raphaelkabo.com/blog/posts/markdown-to-word)，参考流程；
5. [Scrivener for academic writing with Zotero](https://davepwsmith.github.io/academic-scrivener-howto/)，参考流程；
6. [panzer/panzer at master · msprev/panzer](https://github.com/msprev/panzer/tree/master/panzer)，这个可以更多地定义转换的格式，比如行距等。
