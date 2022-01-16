## [MarkDown]() 书写方法

**标题**   #

个数由小到大分为不同等级的标题

```c
/*
#一级标题

##二级标题

###三级标题
*/

```

**2.加粗**   

```c 
//	**加粗内容**
```

​	**加粗内容**



​    

**3.倾斜**    * *

```c
//*这是倾斜*
//***加粗倾斜***
```

*这是倾斜*

***加粗倾斜***



**4.分割线**	

​		在一行中用三个以上的星号、减号、底线来建立一个分隔线，行内不能有其他东西。你也可以在星号或是减号中间插入空格。下面每种写法都可以建立分隔线：

```c
/*
***
**********
_________________
*/
```

***

**********

__________

--------

**5.引用** 

在引用的文字前加 > 即可。 在 Markdown 文件中建立一个区块引用，那会看起来像是你自己先断好行，然后在每行的最前面加上 > ：

```c
/*
>This is a blockquote with two paragraphs. Lorem ipsum dolor sit >amet, consectetuer adipiscing elit. Aliquam hendrerit mi >posuere lectus. Vestibulum enim wisi, viverra nec, fringilla >in, laoreet vitae, risus.
>Donec sit amet nisl. Aliquam semper ipsum sit amet velit. >Suspendisse id sem consectetuer libero luctus adipiscing.
*/
```



>This is a blockquote with two paragraphs. Lorem ipsum dolor sit >amet, consectetuer adipiscing elit. Aliquam hendrerit mi >posuere lectus. Vestibulum enim wisi, viverra nec, fringilla >in, laoreet vitae, risus.
>Donec sit amet nisl. Aliquam semper ipsum sit amet velit. >Suspendisse id sem consectetuer libero luctus adipiscing.

​	Markdown 也允许你偷懒只在整个段落的第一行最前面加上 > ：

要退出就一个回车加shift+tab



**6.列表**

Markdown 支持有序列表和无序列表。 无序列表使用**星号、加号或是减号**作为列表标记。有序列表则使用**数字接着一个英文句点**作为标记。

+ 列表+

* 列表*

- 列表-

列表可以嵌套，上一级和下一级之间tab。

1. 一级有序列表内容 
    1. 二级有序列表
    2. 耳机有序
2. 一级有序列表



**7.表格**

```c
/*
|表头|表头|表头|
---|:--:|---:
内容|内容|内容
内容|内容|内容

第二行分割表头和内容。
- 有一个就行，为了对齐，多加了几个
文字默认居左
-两边加：表示文字居中
-右边加：表示文字居右
注：原生的语法两边都要用 | 包起来。此处省略
*/
```

或者Ctrl+t

| 表头 | 表头 | 表头 |
| ---- | ---- | ---- |
|      |      |      |



**8.代码块**

`单行代码：代码之间分别用一个反引号包起来即可；`

代码之间分别用三个反引号包起来，且两边的反引号单独占一行,且可选择语言



**9.段落和换行**

一个 Markdown 段落是由一个或多个连续的文本行组成，它的前后要有一个以上的空行（空行的定义是显示上看起来像是空的，便会被视为空行。比方说，若某一行只包含空格和制表符，则该行也会被视为空行）。普通段落不该用空格或制表符来缩进。 **我们在两个不同的文字块之间，一定要空行以示区分，不然就会被归入同一文字块中。** Markdown 允许段落内的强迫换行（插入换行符）。 如果想要空一行，在插入处先按入两个以上的空格然后回车，即可。

但有时也可以使用标记来强制空行和空格，比如需要首行缩进的时候： *一个空格大小的表示：\  或 \*  两个空格的大小表示：\ 或 \ *不换行空格：\ 或 \* 强制空行： \



**10.超链接**

要建立一个**行内式**的链接，只要在方块括号后面紧接着圆括号并插入网址链接即可，注意方括号和[圆括号](https://www.zhihu.com/search?q=圆括号&search_source=Entity&hybrid_search_source=Entity&hybrid_search_extra={"sourceType"%3A"article"%2C"sourceId"%3A99319314})之间一定不能有空格，如果你还想要加上链接的 title 文字，只要在网址后面，用双引号把 title 文字包起来即可

` This is a link [](website)`

[百度](www.baidu.com)

除了上面的超链接方式，Markdown 还支持以比较简短的自动链接形式来处理网址和电子邮件信箱，只要是用尖括号包起来， Markdown 就会自动把它转成链接。 语法：

```text
<http://example.com/>
```



**11.插入图片**

 *一个惊叹号 !* 接着一个方括号，里面放上图片的替代文字 * 接着一个普通括号，里面放上图片的网址或本地路径（可以是相对路径或绝对路径），最后还可以用引号包住并加上 选择性的 '标题' 文字。



**12.高亮**

`==高亮==`

==高亮==





