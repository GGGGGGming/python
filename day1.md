# 安装环境
## 安装VNC

    1. [官网](https://www.realvnc.com/en/)
    2. 打开VNC输入服务器的IP地址。

        ![](vnc.png)

## 安装python

   * 到[官网](https://www.python.org/)下载
   * 安装
   * 设置环境变量
        右键点击我的电脑，选择属性，选择高级环境设置，选择环境变量。输入python在此电脑中的地址。
   * 检验是否安装成功

       windows+R，输入cmd，进入命令行界面。输入python，显示如下界面，安装成功。

       ![](python.png)




      python 版本

	序号	|	版本名称	|	备注
	---	|	---		|	---
    01	|	python3.x|	继续

## 安装pycharm

   * 到[官网](http://www.jetbrains.com/pycharm/)下载
   * 安装

       选择试用30天
   * 检验是否安装成功

       双击JetBrains PyCharm 2018.1.2 x64，进入主界面，安装成功。

# 基础语法
1. python全景

    1. 程序由模块组成
    2. 模块包含语句
    3. 语句包含表达式
    4. 表达式建立并处理对象
2. 中文编码

    只要在文件开头加入# -    *   - coding:utf-8 -*-

	
      	#-*- coding:utf-8 -*-
	> python3.x默认使用utf-8编码。
	> 
	> python与数据库编程编码需一致
3. python标识符

	* 标识符由字母数字和下划线组成。
	* 开头可以是英文，下划线，不能以数字开头
	* 下划线开头的名字都有特殊的含义
	* 多数选择英文加下划线再加英文
	
4. 行和缩进

	python语言不使用{}来控制类和函数，这也python最大的特色，就是使用缩进来写模块。
	> 每个缩进层次都要使用单个制表符，不要使用空格。

5. 多行语句
	* python语句一般以新行作为语句的结束符
	* 也可以使用斜杠（\）将一行语句多行显示：
	* 
			total = item_one + \
    		item_two + \
    		item_three

6. 注释单行用#开头，多行注释用三个单引号或三个双引号。
	
7. 输入默认换行
	
#创建名片

* 使用输入和输出
* 不同的类型需要用不同的标识符
* 代码并不完美，如果输入hh，将会出现错误
* 
		print('你好')
		name = input('你的名字叫:')
		phone = int(input('你的电话是:'))
		company = input('你的公司叫:')
		print('===================')
		print('姓    名:%s' % (name))
		print('电    话:%d' % (phone))
		print('公司名称:%s' % (company))
		print('===================')
## 输出结果如下图所示：![](https://i.imgur.com/XeR2Fe0.png)


# 导入模块
## 导入sys模块
1. import sys
2. print sys
3. 如果输出没有错误，则导入成功。

#if语句
## 两个条件的if语句
	if age<18:
		print('你还小')
    else:
		print('你挺大阿')
## 三个条件的if语句
	age=int(input('请输入你得年龄：'))
	if age>=80:
    	print("太大了吧")
	elif 18<=age<80:
    	print('恭喜恭喜')
	else:
    	print('小孩还是稍稍')


   





