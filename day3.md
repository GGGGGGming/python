##变量类型String
1. 变量分为可变性和不可变性两种，数字、字符串和元组是不可变性；列表和字典是可变性变量。

		s='python' s[0]='p'#error
2. 单引号和双引号等价，可以嵌套使用

		print('i love "python"')
		print("i love 'python'")
3. 三引号包含多行字符串常量，所有行合并在一起，并在每行末尾增加一个换行符，doc当把三引号字符串放在代码开始时，可以通过下面两种方式输出：
		
		 ```
   		 """
          line 1 hello
          line2
          line3'''line3-content'''
          <html>
                <body></body>
          </html>

    	"""
    	#命令行
    	python test.py __doc__

   	 	#代码文件中

	    print(__doc__)
		```
	>必须放在第一行，每个文件只能有一条\

4. 转义字符
	1. 续行符
	
	a=12 b=12 c=10 d=a+\b+\c
	print(d)

	2.raw字符串

	myfile=open('c:\new\text.dat') #这里\n \t 会被认为是转义字符，为了解决可以这么写 myfile=open(r'c:\new\text.dat') myfile=open('c:\new\text.dat')
5. Python字符串

	python的字串列表有两种取值顺序：
	
	1.从左到右索引默认为0
	2.从右到左索引默认为-1。获取一部分字符串可以使用变量[头下标，尾下标]，就可以截取相应的字符串。如果头下标不写，就重头开始切，如果尾下标不写，就切到最后。尾下标中不包含尾下标的内容。-1是最后一个空。当最后的跳跃间隔不是负的时，不能反方向切。
	例如：

		# s='python'
		# print(s[0:2])结果就是'py'
		# print(s[::2])结果就是'pto'
		# print(s[::-1])结果就是'nohtyp'

6. 字符串输出
	
	格式化符号说明备注%s字符串输出string10s右对齐，占位符10位-10s左对齐，占位符10位%.2s截取2位字符串%10.2s10位占位符，截取两位字符。*表示字符串的重复，支持不同的类型，+表示字符串的连接，只能相同类型连接。
	>字符串不可更改，更换标识符时，系统中小于512的数字会留存一段时间，大于512的数字就根本不会保留，字符串同理，由数字字母下划线组成的字符串可以储存。

7. 内建函数
    1. 统计单词出现的次数
    
        ```
            str='hello world hello china'
    
            num=str.count('hello',0,len(str))
    
            print(num)
        ```
    
    2. find()

        ```
            word='hello python,hello,world'

            res01=word.find('hello',4,8)
        ```
    3. replace

        ```
            word='hello python,hello,world'
            res02=word.replace('hello','hi',2)
        ```
    4. split()
    5. join()

        ```
            arr=list(word)

            str_arr=','.join(arr)
            print(str_arr)
            str2='python'.join(['_one_','_two_','_three_'])
        ```
    5. upper() lower()
    6. strip() lstrip() rstrip() len
8. 总结
	1. len长度
	2. for...in..循环
	3. {0}.fomat
	4. 切片
	5. 内建函数类型：	
	
			strip去空格，
			split切断，
			count统计，
			find查找，
			replace代替，
			isdigit数字类型，
			Isalpha字母类型，
			isalnum数字和字母类型

#变量类型-list
## list
1. 列表的数据项不需要相同类型

2. list是Python中使用最频繁的数据类型

3. 列表可以完成大多数集合类的数据结构实现，它支持字符，数字，字符串甚至包含列表。既嵌套。
##列表取值
1. 列表中值的切割也可以用到变量[头下标:尾下标]，就可以截取相应的列表，从左到右索引默认0开始，从右到左索引默认-1开始，下标可以为空表示取到头或尾。
2. +是列表连接运算符，*是重复操作

		list=[1,2,5,6,7,8,10]
		输出第一个元素print list[0]
		输出第二个到第三个元素print list[1:3]
		输出第四个元素到最后一个元素print list[4:]
##list操作
list01=['1','3','5','6','7','8','9','10']

1. 统计

		print(list01.count('1'))
2. 判断是否存在

		print(list01.count('1'))
3. 反转整个数组
		
		list01.reverse()
		print (list01)
		输出结果为'10','9','8','7','6','5','4','3','2','1'
>可对列表本身进行反转，但不建议这么做，可以将列表赋予一个新的标识符进行操作，便于返回本身。

4. 对数组进行排序
		
		list01.sort()
		printt(list01)
>注意事项和反转相同。

		