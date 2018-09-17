#变量类型-list

1. 列表操作

		增加元素：fruits.append('kiwi')
		增加集合：fruits.extend('kiwi','water')
		合并两个列表：new_fruits=fruits+['kiwi','water']
		插入元素：fruits.insert(0,'pick');
		删除元素：fruits.remove('apple'),del fruits[1]
		删除单个元素：fruits[1:2]=[]
		删除多个元素：fruits[2:4]=[]
		删除聊表末尾的元素：fruits.pop()
		判断是否存在：print('apple'in fruits)
		最大最小值：print(max(fruits)),print(min(fruits))

	>列表中追加的元素只能是集合。
	>pop可以把最上面（最右）的元素弹出

2. 	栈和队列

		
	队列在使用前需要先导入，from collections import deque只导入队列。
		
		list02=list(queue_list01)
 	>上述代码可将队列变回数组。

	>队列是先进先出，栈是先进后出
 	
3. map
	
	第一个参数 function 以参数序列中的每一个元素调用 function 函数，返回包含每次 function 函数返回值的新列表。
	
		map(funtion,iterable,.....)
#变量类型-Tuple
1. tuple内容不可以改变，相对来说比较安全，如果需要改变的话，先转换成数组再根据需要进行更改，更改完之后再进行转换成为tuple类型。


#二维数组

exp：

	books=[['三国演义'],['西游记'],['三国志'],['三国杀'],['水浒传']]

二维数组的某一列排序
	
	arr=[]
	for i in range(len(books)):
		li=[books[i][2],i]
		arr.append(li)
	arr.sort()
	print(arr)
	
	result_list=[]
	for item in arr:
		i=item[1]
		
		result_list.append(books[i])

	print(result_list)

#排序

##选择排序法

	#选择排序法
	list01=[6,4,8,7,9,23,15,16,19,99,18,1,2,5]
	le=len(list01)
	i=0
	while i<le-1:
    	j=i+1
    	w=i
    	while j<le:
        	if list01[w]>list01[j]:
            	w=j
        	j=j+1
    	t=list01[i]
    	list01[i]=list01[w]
    	list01[w]=t
    	i+=1
	print(list01)

##冒泡排序法

	#冒泡排序
	list01=[6,4,8,7,9,23,15,16,19,99,18,1,2,5]
	i=0
	le=len(list01)
	while i<le-1:
    	j=0
    	while j<le-1-i:
        	if list01[j]>list01[j+1]:
        	    t=list01[j]
        	    list01[j]=list01[j+1]
        	    list01[j+1]=t
        	j=j+1
    	i=i+1
	print(list01)


#复习

##数组访问
1. 数组初始化
2. 输出单个元素
3. 数组重新赋值
4. 数组遍历

		for i in list01

##数据截取
1. 截取第一个
 
		list01[0]
2. 截取最后一个

		list01[-1]
3. 截取三到五个

		list01[3:6]
4. 截取三到最后一个

		list01[3:]
5. 截取所有

		list01[:]
6. 数组反转

		list01[::-1]
##数据处理

1. 数组反向排序

		list01.sort(reverse=True)
2. 数组求和

		sum(list01)
3. 数组最大值

		max(list01)
4. 数组最小值
	
		min(list01)
5. 数组平均值

		sum(list01)/len(list01)
6. 验证是否存在

		list01.index(5)
		list01.count(5)
		5 in list01
7. 清空数组

		list01.clear
8. 删除

		list01.remove()
		del list01
