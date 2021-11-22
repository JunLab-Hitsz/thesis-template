# 哈工大毕业论文模板
该仓库为哈工大深圳毕业模板，改模板由[hithesis](https://github.com/dustincys/hithesis)的代码生成。

## Debug List

- 修复在windows下，封面生僻字无法显示的bug

该问题的主要原因是该latex模板默认使用fandol字体，该字体不能很好显示"鋆"，在`thesis.tex`文件中设置字体`fontset=windows`即可解决该问题。(该模板已经默认修改为了windows字体)

- 修改封面内容，符合2021年要求。[2021论文规范](http://due.hitsz.edu.cn/info/1247/2735.htm)

- 去除页眉

查重时，页眉可能也会出现重复情况，有去除页眉的需求。方法如下:
注释掉`*.cls`文件中关于页眉的定义部分(约361行附近):
```
\fancypagestyle{hit@headings}{%
    ...
    \else
      \ifhit@master
        \ifhit@harbin
          \fancyhead[C]{\songti\xiaowu[0]\hit@cschoolname\hit@cdegree\hit@cthesisname}
        \fi
        \ifhit@shenzhen
          \if@mainmatter
            % 注释如下一行
            % \fancyhead[C]{\songti\xiaowu[0]\hit@cschoolname\hit@cdegree\hit@cthesisname}
          \else
            \fancyhead[C]{\xiaowu[0]\leftmark}
          \fi
        \fi
    ...
}
```




# Reference

- https://github.com/dustincys/hithesis