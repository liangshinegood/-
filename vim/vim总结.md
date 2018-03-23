# 1.参考资料 #
	1.自己购买的资料：
	[http://www.ydma.com/classroom/14/task/65](http://www.ydma.com/classroom/14/task/65)

	2.简明 VIM 练级攻略
	[https://coolshell.cn/articles/5426.html](https://coolshell.cn/articles/5426.html)

	3.高效率编辑器 Vim——操作篇，非常适合 Vim 新手
	[https://linuxtoy.org/archives/efficient-editing-with-vim.html](https://linuxtoy.org/archives/efficient-editing-with-vim.html)

	4.vim操作全面讲解
	[http://www.cnblogs.com/hustskyking/archive/2013/06/11/linux-learning-details.html](http://www.cnblogs.com/hustskyking/archive/2013/06/11/linux-learning-details.html)
	

# 2.学习总结 #
	
	**首先是我所熟悉的几个**：
	a,i,o,gg,yy,u,ctrl+r,co,m,s/^/#/g，s/^#//g,dd,p,set nu
	H,$，/，？

----------

	配置vim:~/.vimrc中

	
----------
	光标的移动：f+x(代表你想要的字符)很有用，（上下左右）
	“  ） ”光标的下一句
	“ （  ”光标的上一句

	ma：在当前光标的位置标记一个书签，名字为 a。书签名只能是小写字母。你看不见书签的存在，但它确实已经在那里了。

	`a：到书签 a 处。注意这个不是单引号，它一般位于大部分键盘的 1 的左边。

	`.：到你上次编辑文件的地方。这个命令很有用，而且你不用自己去标记它。

----------

	使用关键词自动完成功能，你只需要输入开始几个字母（比如 iAmAL），然后按 <C-N>（**按住 Ctrl，再按 N）**或者 <C-P>。如果 Vim 没有给出你想要的词，继续按，直到你满意为止，Vim 会一直循环它找到的匹配的字符串。

----------

	**使用可视选择（visual selections）和合适的选择模式**

	不像最初的 VI，Vim 允许你高亮（选择）一些文本，并且进行操作。这里有三种可视选择模式：
	
	v：按字符选择。经常使用的模式，所以亲自尝试一下它。
	V：按行选择。这在你想拷贝或者移动很多行的文本的时候特别有用。
	<C-V>：按块选择。非常强大，只在很少的编辑器中才有这样的功能。你可以选择一个矩形块，并且在这个矩形里面的文本会被高亮。

	一旦你高亮了选区，你或许想进行一些操作：
	
	d：剪贴选择的内容到剪贴板。
	y：拷贝选择的内容到剪贴板。
	c：剪贴选择的内容到剪贴板并且进入插入模式。

----------

	
	**Vim 是一个用来写代码的绝好编辑器**，因为它有一些特性是专门为程序员而设计的。这里是一些常用的：
	
	]p：和 p 的功能差不多，但是它会自动调整被粘贴的文本的缩进去适应当前代码的位置。试一下！

	%：匹配花括号、方括号、括号等。在一个括号的上面，然后按 %，鼠标就会出现在匹配的另外一半括号处。

	>>：缩进所有选择的代码
	
	<<：和上面类似，但是反缩进

	gd：到达光标所在处函数或者变量的定义处。

	K：在 Man 里面查找光标当前所在处的词。	


# 3.问题记录及解决 #