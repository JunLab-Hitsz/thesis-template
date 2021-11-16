# 哈工大毕业论文模板
该仓库为哈工大深圳毕业模板，修改自[hithesis](https://github.com/dustincys/hithesis )latex模板。



## Debug List

- 修复封面生僻字无法显示的bug

该问题的主要原因是该latex模板使用siyuan字体，该字体不能很好显示"鋆"，为了解决这个问题，将`hithesis.cls`文件中122行附近的如下片段注释。

```tex
% 需要注释掉下面字体设置才能正常显示一些生僻字，如鋆
% {%
%   \ifthenelse%
%   {\equal{\hit@fontset}{siyun}}%
%   {\relax}%
%   {%
%     \PassOptionsToPackage{AutoFakeBold=2}{xeCJK}
%   }%
%   \PassOptionsToClass{fontset=\hit@fontset}{ctexbook}
% }%
```

- 修改封面内容，符合2021年要求。[2021论文规范](http://due.hitsz.edu.cn/info/1247/2735.htm)



# Reference

- https://github.com/dustincys/hithesis