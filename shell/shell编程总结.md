# 1. 资源参考 #
	1.网上购买的学习教程
	[http://www.ydma.com/classroom/14/task/65](http://www.ydma.com/classroom/14/task/65)

	2.菜鸟学院资料
	[http://www.runoob.com/linux/linux-tutorial.html](http://www.runoob.com/linux/linux-tutorial.html)
	


# 2. 学习总结 #
	在linux操作的基础上，增加一些shell编程脚本，可以批量的处理系统


----------
	
	**变量**：直接输入名称，如：your_name="runoob.com",命名规范同一般语言
	使用变量：echo $your_name
	只读变量：前面加上 **readonly** your_name
	删除变量：前面加上 **unset** your_name
	字符变量：（拼接，获取长度，提出子字符，查找）
	your_name='qinjx'
	str="Hello, I know your are \"$your_name\"! \n"
	
	拼接总结：引号括起来，$+变量
	your_name="qinjx"
	greeting="hello, "$your_name" !"
	greeting_1="hello, ${your_name} !"
	echo $greeting $greeting_1
	
	长度总结：大括号，加“#”，加变量
	string="abcd"
	echo ${#string} #输出 4

	提取子字符总结：大括号，加变量，加：1：4
	string="runoob is a great site"
	echo ${string:1:4} # 输出 unoo
	
	查找变量元素总结：反引号``
	string="runoob is a great company"
	echo `expr index "$string" is`  # 输出 8
	注意： 以上脚本中 "`" 是反引号，而不是单引号 "'"，不要看错了哦

----------

	**数组**：array_name=(value0 value1 value2 value3)
	# 取得数组元素的个数
	length=${#array_name[@]}
	# 或者
	length=${#array_name[*]}
	# 取得数组单个元素的长度
	lengthn=${#array_name[n]}
	

	以"#"开头的行就是注释，会被解释器忽略

----------

	**shell传递参数**
	脚本：
	echo "Shell 传递参数实例！";
	echo "第一个参数为：$1";
	
	echo "参数个数为：$#";
	echo "传递的参数作为一个字符串显示：$*";

	执行脚本：
	$ chmod +x test.sh 
	$ ./test.sh 1 2 3
	Shell 传递参数实例！
	第一个参数为：1
	参数个数为：3
	传递的参数作为一个字符串显示：1 2 3

----------

	**$* 与 $@ 区别：**
	相同点：都是引用所有参数。
	不同点：只有在双引号中体现出来。假设在脚本运行时写了三个参数 1、2、3，，则 " * " 等价于 "1 2 3"（传递了一个参数），而 "@" 等价于 "1" "2" "3"（传递了三个参数）

----------

	**运算符号**
	总结：``反引号，expr , $a (符号) $b
	a =10 b = 20
	val=`expr $a + $b`
	echo "a + b : $val"
	
	val=`expr $a - $b`
	echo "a - b : $val"
	
	val=`expr $a \* $b`
	echo "a * b : $val"
	
	val=`expr $b / $a`
	echo "b / a : $val"
	
	val=`expr $b % $a`
	echo "b % a : $val"


----------
	
	**逻辑if[条件] then 语句 fi**

----------

	if [ $a -eq $b ] a 等于 b"
	if [ $a -ne $b ] a 不等于 b"
	if [ $a -gt $b ] a 大于 b"
	if [ $a -ge $b ] a 大于或等于 b"
	if [ $a -lt $b ] a 小于 b"
	if [ $a -le $b ] a 小于或等于 b"
	if [ $a != $b ] a 不等于 b"
	if [ $a -lt 100 -a $b -gt 15 ] a 小于 100 且 $b 大于 15
	if [ $a -lt 100 -o $b -gt 100 ] a 小于 100 或 $b 大于 100 
	if [[ $a -lt 100 && $b -gt 100 ]] 
	if [[ $a -lt 100 || $b -gt 100 ]]
	if [ $a ]字符串不为空
	if [ -n $a ] 字符串长度不为 0"
	if [ -z $a ] 字符串长度为 0
	if [ $a = $b ] a 等于 b"
	file="/var/www/runoob/test.sh"
	if [ -r $file ] "文件可读"
	if [ -w $file ] "文件可写
	if [ -x $file ] "文件可执行"
	if [ -f $file ]文件为普通文件"
	if [ -d $file ] 文件是个目录"
	if [ -s $file ] 文件不为空
	if [ -e $file ] 文件存在
	
	if [ $a == $b ]
	then
	   echo "a 等于 b"
	fi
	if [ $a != $b ]
	then
	   echo "a 不等于 b"
	fi

----------

	**echo "It is a test" > myfile**


----------
	
	Shell中的 test 命令用于检查某个条件是否成立，它可以进行数值、字符和文件三个方面的测试

	**FOR ，until，while 循环**
	for loop in 1 2 3 4 5
	do
	    echo "The value is: $loop"
	done

----------
	**ase语句为多选择语句**
	echo '输入 1 到 4 之间的数字:'
	echo '你输入的数字为:'
	read aNum
	case $aNum in
	    1)  echo '你选择了 1'
	    ;;
	    2)  echo '你选择了 2'
	    ;;
	    3)  echo '你选择了 3'
	    ;;
	    4)  echo '你选择了 4'
	    ;;
	    *)  echo '你没有输入 1 到 4 之间的数字'
	    ;;
	esac
	

----------

	**函数**
	demoFun(){
	    echo "这是我的第一个 shell 函数!"
	}
	echo "-----函数开始执行-----"
	demoFun
	echo "-----函数执行完毕-----"

	funWithParam(){
	    echo "第一个参数为 $1 !"
	    echo "第二个参数为 $2 !"
	    echo "第十个参数为 $10 !"
	    echo "第十个参数为 ${10} !"
	    echo "第十一个参数为 ${11} !"
	    echo "参数总数有 $# 个!"
	    echo "作为一个字符串输出所有参数 $* !"
	}
	funWithParam 1 2 3 4 5 6 7 8 9 34 73


----------
	
		输出、输出重定向
		$ echo "www.runoob.com" > users
		$ cat users
		www.runoob.com
		
		$ echo "www.runoob.com" >> users
		$ cat users
		www.runoob.com
		www.runoob.com
		$
		$ wc -l users
		       2 users
		
		$ wc -l << EOF
		    欢迎来到
		    www.runoob.com
		EOF
		3          # 输出结果为 3 行
		$

----------

	**/dev/null 文件**
	如果希望执行某个命令，但又不希望在屏幕上显示输出结果，那么可以将输出重定向到 /dev/null：
	$ command > /dev/null

----------

	**执行文件**
	$ chmod +x test2.sh 
	$ ./test2.sh 
	http://www.runoob.com

history,alias,wc,netstat -an|grep ESTABLISHED

# 3. 遇到的问题 #