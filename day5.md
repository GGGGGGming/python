#数据类型-Set
##集合简介
1. 集合是一个无序不重复的序列，可以使用｛｝或set（）函数创建集合。
2. 创建空的集合不可以只使用｛｝，如果只用｛｝会创建出一个空的字典
3. 想要给数组去重，可以先将数组变成集合类型，自动进行去重，再将集合转换成数组类型，就可以正常输出了。

		a-b #集合a中包含元素
		a|b #集合a或b中包含的所有元素
		a&b #集合a或b中都包含了的元素
		a^b #不同时包含于a和b的元素
##集合的基本操作
###添加元素
将元素添加到s中，如果元素已存在，则不进行任何操作。

	s.add(x)
还有另一种方法，x可以有多个，但是要用逗号分开。将字符串拆分单个字符后，然后在一个个添加到集合中，有重复的会忽略。

	s.update(x)
###移除元素
将元素x添加到s中移除，如果元素不存在，则会发生错误。

	s.remove(x)
此外还有一个方法，如果元素不存在，不会发生错误。
	
	s.disacard(x)
可以随机删除集合中的一个元素，

	s.pop()
###计算集合元素个数
集合s元素个数

	len(s)
###清空集合
清空集合s

	s.clear
###判断元素中集合是否存在

	x in s

>题外话，储存年龄是可选择储存生日，这样不会随着年龄变化而变化。

#数据类型-Dictionary

1. 类型字典每个key对应着一个value，之间用冒号隔开，每个键值对之间用逗号分割，整个字典包括在花括号中。键是唯一的，但是值不一定是唯一的。
2. 字典与列表，原组一样，都是可以遍历的。
3. 字典访问

	
	  	user={
	    'name':{'firstName':'zhan','lastName':'liang'},
	    'age':20,
	    'address':'usa',
	    'hobby':['film','sport']
	    }
	
	    print('user length:',len(user))
	
	    print('user first property is :',user['name'])
	    
	    for key,value in user.items():
	        print ('property %s value  %s' % (key,value))
	    
	    for kk in user.keys():
	        print ('property %s' % (kk))
	    
	    for vv in user.values():
	        print ('values %s' % (vv))

4. 访问不存在的键，访问会错误。
5. 新增，修改字典内的内容

		dict = {'Name': 'Runoob', 'Age': 7, 'Class': 'First'}
	 
		dict['Age'] = 8;               # 更新 Age
		dict['School'] = "菜鸟教程"  # 添加信息
	 
	 
		print ("dict['Age']: ", dict['Age'])
		print ("dict['School']: ", dict['School'])
6. 字典内置函数



		len(dict)#计算字点元素个数，即键的个数。
	 	str(dict)#输出字典，以可打印的字符串表示。
		type(variable)#返回输入的变量类型，如果变量是字典就反悔字典类型。
7. 字典内置函数

	1. radiansdict.clear()#删除字典内所有元素
	2. radiansdict。copy()#返回一个字典的潜复制
	3. radiansdict.fromkeys()#创建一个新的字典，
	4. radiansdict.get(key,default=None)#返回指定的值
	5. key in dict
如果键在字典dict里返回true，否则返回false
	6. radiansdict.items()
以列表返回可遍历的(键, 值) 元组数组
	7. 	radiansdict.keys()
以列表返回一个字典所有的键
	8. radiansdict.setdefault(key, default=None)
和get()类似, 但如果键不存在于字典中，将会添加键并将值设为default
	9. radiansdict.update(dict2)
把字典dict2的键/值对更新到dict里
	10. radiansdict.values()
以列表返回字典中的所有值
	11. pop(key[,default])
删除字典给定键 key 所对应的值，返回值为被删除的值。key值必须给出。 否则，返回default值。
	12. popitem()
随机返回并删除字典中的一对键和值(一般删除末尾对)。