![](https://github.com/kuileiguai/DM.exe/blob/main/image/20220915172232914.png)
[TOC]
# 1 背景
在金赋开发者社区发布1.0版本后，将会有大量的文档需要添加到书架中，但社区中图书的文件为Markdown文件，这使得docx文件不能直接添加到开发者社区，因此，这里开发了一款用于将docx文件转换为Markdown文件的工具。
# 2 准备
## 2.1 Windows系统安装
### 2.1.1 安装JDK8
下载地址：
下载jdk-8u341-windows-x64.exe
(1) 运行jdk-8u341-windows-x64.exe，点击确定
![](https://github.com/kuileiguai/DM.exe/blob/main/image/20220915172232932.jpeg)
(2) 点击更改可以选择安装路径，选择完成后记住安装的路径，点击下一步
![](https://github.com/kuileiguai/DM.exe/blob/main/image/20220915172232948.jpeg)
(3) 安装中......
![](https://github.com/kuileiguai/DM.exe/blob/main/image/20220915172232968.jpeg)
(4) 安装完成，点击关闭
(5) 运行环境变量配置工具（二选一）
![](https://github.com/kuileiguai/DM.exe/blob/main/image/20220915172232984.png)
(6) 选择找到刚刚安装时的路径，点击设置，设置成功即可
![](https://github.com/kuileiguai/DM.exe/blob/main/image/202209151722332.png)
(7) 查看jdk是否安装成功
按win + r调出运行窗口，输入cmd调出命令行窗口
![](https://github.com/kuileiguai/DM.exe/blob/main/image/2022091517223317.png)
在命令行中输入java -version后，如果看到如下，则安装jdk成功
![](https://github.com/kuileiguai/DM.exe/blob/main/image/2022091517223335.png)
### 2.1.2 安装Pandoc
下载地址：<https://www.pandoc.org/installing.html>
(1) 下载后双击安装程序
![](https://github.com/kuileiguai/DM.exe/blob/main/image/2022091517223347.png)
(2) 勾选全部，点击Install
![](https://github.com/kuileiguai/DM.exe/blob/main/image/2022091517223364.png)
(3) 等待......
![](https://github.com/kuileiguai/DM.exe/blob/main/image/2022091517223381.png)
(4) 点击Finish完成安装
![](https://github.com/kuileiguai/DM.exe/blob/main/image/2022091517223399.png)
## 2.2 Mac系统安装
### 2.2.1 安装JDK8
下载地址：
(1) 运行下载的安装包,一直点击继续
![](https://github.com/kuileiguai/DM.exe/blob/main/image/20220915172233117.png)
![](https://github.com/kuileiguai/DM.exe/blob/main/image/20220915172233135.png)
![](https://github.com/kuileiguai/DM.exe/blob/main/image/20220915172233152.png)
(2) 运行终端输入java -version查看是否安装成功
![](https://github.com/kuileiguai/DM.exe/blob/main/image/20220915172233171.png)
### 2.2.2 安装Pandoc
下载地址:https://www.pandoc.org/installing.html
![](https://github.com/kuileiguai/DM.exe/blob/main/image/20220915172233188.png)
(1) 运行安装包
![](https://github.com/kuileiguai/DM.exe/blob/main/image/20220915172233219.png)
(2) 点击继续
![](https://github.com/kuileiguai/DM.exe/blob/main/image/20220915172233237.png)
(3) 点击同意
![](https://github.com/kuileiguai/DM.exe/blob/main/image/20220915172233253.png)
(4) 点击安装
![](https://github.com/kuileiguai/DM.exe/blob/main/image/20220915172233269.png)
(5) 关闭
![](https://github.com/kuileiguai/DM.exe/blob/main/image/20220915172233285.png)
# 3 运行
## 3.1 Windows上运行
1.  下载DM_64bit.exe (下载地址:
    [https://github.com/kuileiguai/DM.exe](https://github.com/kuileiguai/DM.exe.git))
2.  下载后可放在任何位置
![](https://github.com/kuileiguai/DM.exe/blob/main/image/20220915172233303.png)
3.  双击.exe即可运行
## 3.2 Mac上运行
开发中
# 4 文档优化
## 4.1 目录的优化
在开发过程中，我们发现docx文档中原有目录的样式会影响到转换后的匹配度，为了能够令转换的准确度变高，建议在文档编写完成后，采用自动生成目录得到文档目录。
### 4.1.1 采用自动生成目录
![](https://github.com/kuileiguai/DM.exe/blob/main/image/20220915172233328.png)
![](https://github.com/kuileiguai/DM.exe/blob/main/image/20220915172233348.png)
按照自动目录的形式生成目录，会得到以下形式的目录
![](https://github.com/kuileiguai/DM.exe/blob/main/image/20220915172233365.png)
在转化为Markdown文件后，会有如下的形式：
目录标签：
![](https://github.com/kuileiguai/DM.exe/blob/main/image/20220915172233382.png)
这种方式形式的目录是工具能够处理的。
## 4.2 标题的优化
在插入标题时，确保标题中拥有标签并且标签成立：
标签成立时，当鼠标单击标签，会使标签得到全选中
![](https://github.com/kuileiguai/DM.exe/blob/main/image/20220915172233399.png)
这种标签是不成立的
![](https://github.com/kuileiguai/DM.exe/blob/main/image/20220915172233417.png)
## 4.3 表格的优化
在开发过程中，我们发现docx文档中表格转换成markdown文件后，会出现两种形式。
### 4.3.1 转换表格类型一
文档中表格：
![](https://github.com/kuileiguai/DM.exe/blob/main/image/20220915172233434.png)
转换后形式：
![](https://github.com/kuileiguai/DM.exe/blob/main/image/20220915172233452.png)
出现的条件：当表格中各单元格文本能在格内一行写完，未在格内出现换行情况，则会出现这种转换情况，由于这类型表格十分常见，在这里工具也实现了对这种表格类型的部分处理。
满足处理的条件是：单元格内文本未出现空格，除末列单元格外，其余单元格不能有空。
### 4.3.2 转换表格类型二
文档中表格;
![](https://github.com/kuileiguai/DM.exe/blob/main/image/20220915172233469.png)
转换后形式：
![](https://github.com/kuileiguai/DM.exe/blob/main/image/20220915172233487.png)
出现的条件：当表格中部分单元格文本出现格内换行情况，则会出现这种转换情况，这种形式的转换能够十分清晰的知道各单元格内文本内容。
满足处理的条件是：单元格内文本未出现空格，部分单元格格内文本出现换行。
### 4.3.3 处理复杂表格
当出现这种表个情况时，应该如何处理？
转换前：
![](https://github.com/kuileiguai/DM.exe/blob/main/image/20220915172233505.png)
转换后：
![](https://github.com/kuileiguai/DM.exe/blob/main/image/20220915172233523.png)
情况分析：由于markdown文件中不存在单元格合并这种表格格式，因此会出现这种十分混乱的转换，并且这种表格中有空白单元格转换工具无法正确还原出原有表格。
解决方法：此时可以在表格第一行中的单元格内人工进行换行操作。
![](https://github.com/kuileiguai/DM.exe/blob/main/image/20220915172233540.png)
转换后：
![](https://github.com/kuileiguai/DM.exe/blob/main/image/20220915172233557.png)
![](https://github.com/kuileiguai/DM.exe/blob/main/image/20220915172233578.png)
当然，先前改动的第一行的单元格内内容也需要人工更正，但这比起整个复杂表格而言，是微不足道的。
## 4.4 图片的优化
图片格式一般为常见的.png,.jpeg,.jpg;但开发中也会发现会有.emf格式的存在，这两大类图片格式在转换后的区别在与宽高参数的有无。
.png,.jpeg,.jpg
![](https://github.com/kuileiguai/DM.exe/blob/main/image/20220915172233594.png)
.emf
![](https://github.com/kuileiguai/DM.exe/blob/main/image/20220915172233612.png)
因此，为保证图片能准确转换成可上传到开发者社区的形式，需要保证当前要转换文档所在的路径上没有空格、括号、以及特殊字符。
## 4.5 其他优化
在撰写文档时，要习惯回车后写新行的内容，不要指望于wps中的自动换行，因为视觉上已经完成了换行，但本质上还处在同一行中，这样会给转换带来一些未知的因素。
# 5 Q&A
