# machine-learning-yearning 中文翻译PDF优化版和Epub版
## 简介
本项目为NG的手稿的官方授权翻译的PDF优化版以及Epub版。

[官方授权翻译地址](https://github.com/deeplearning-ai/machine-learning-yearning-cn)  
[在线阅读地址](https://deeplearning-ai.github.io/machine-learning-yearning-cn/)

鉴于官方授权翻译放出来的PDF字体观感不好，特地使用官方授权翻译仓库内的翻译内容，用pandoc导出成tex格式微调后，用latex编译的PDF版本。以及导出成了Epub版本，方便在电子书上阅读。

## 导出方式：
### PDF
1. 导出TEX  
    进入doc中，用pandoc导出成tex
    ```bash
    pandoc ch01.md ch02.md ch03.md ch04.md ch05.md ch06.md ch07.md ch08.md ch09.md ch10.md ch11.md ch12.md ch13.md ch14.md ch15.md ch16.md ch17.md ch18.md ch19.md ch20.md ch21.md ch22.md ch23.md ch24.md ch25.md ch26.md ch27.md ch28.md ch29.md ch30.md ch31.md ch32.md ch33.md ch34.md ch35.md ch36.md ch37.md ch38.md ch39.md ch40.md ch41.md ch42.md ch43.md ch44.md ch45.md ch46.md ch47.md ch48.md ch49.md ch50.md ch51.md ch52.md ch53.md ch54.md ch55.md ch56.md ch57.md ch58.md -o tmp.tex
    ```
2. 修改TEX
    1. 然后修改导出的tex中的标题，将`subsection`替换成`chapter`，将`section`替换成`part`
    2. 修改图片文件地址`../img`为`./img`
3. 编译  
   将修改好的TEX文件移动到外面目录，然后修改`MLY.tex`里嵌入的tex文件名称。然后进行编译  
   下面命令运行两遍
   ```bash
   xelatex MLY.tex
   ```
### EPUB
epub格式可以直接导出  
进入doc文件夹，然后运行一下命令：  
```bash
pandoc ch01.md ch02.md ch03.md ch04.md ch05.md ch06.md ch07.md ch08.md ch09.md ch10.md ch11.md ch12.md ch13.md ch14.md ch15.md ch16.md ch17.md ch18.md ch19.md ch20.md ch21.md ch22.md ch23.md ch24.md ch25.md ch26.md ch27.md ch28.md ch29.md ch30.md ch31.md ch32.md ch33.md ch34.md ch35.md ch36.md ch37.md ch38.md ch39.md ch40.md ch41.md ch42.md ch43.md ch44.md ch45.md ch46.md ch47.md ch48.md ch49.md ch50.md ch51.md ch52.md ch53.md ch54.md ch55.md ch56.md ch57.md ch58.md -o MLY.epub --metadata title="MLY" --metadata cover-image="../img/index.jpg"
```