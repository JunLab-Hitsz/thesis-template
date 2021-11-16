# 哈工大毕业论文模板
该仓库为哈工大深圳毕业模板，改模板由[hithesis](https://github.com/dustincys/hithesis)的代码生成。

## Debug List

- 修复在windows下，封面生僻字无法显示的bug

该问题的主要原因是该latex模板默认使用fandol字体，该字体不能很好显示"鋆"，在`thesis.tex`文件中设置字体`fontset=windows`即可结局该问题。(该模板已经默认修改为了windows字体)

- 修改封面内容，符合2021年要求。[2021论文规范](http://due.hitsz.edu.cn/info/1247/2735.htm)



# Reference

- https://github.com/dustincys/hithesis