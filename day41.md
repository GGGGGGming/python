#JQuery

##jQuery基础
>用更少的代码，做更多的事情。
###this的作用
1. this表示当前作用域下的对象
2. 在函数中指向windows
3. 在方法中指向调用该方法的对象。

###对象类型的判断
1. typeof函数：返回对象的具体类型
2. instanceof：判断对象是否是某种类型的实例。

###构造方式总结
1. 构造方法依靠this关键字实现属性的设置。
2. 构造方法通过new关键字创建实例对象。

###jQuery基础语法
1. $（document）.ready()与window.onload类似，但也有区别。
2. $(selector).action();$等于jQuery

###DOM对象和jQuery对象
1. DOM：直接使用js获取的节点对象
2. jQuery：使用jQuery包装DOM对象后产生的对象，它能够使用jQuery的方法。
3. DOM和jQuery分别拥有一套独立的方法，不能混用。

###jQuery对象转DOM对象
1. jQuery对象是一个类似数组的对象，可以通过index的方法得到相应的DOM对象。
```
var $txtName=$('#txtName');
var txtName=$txtName[0];
```
2. 通过get（index）方法得到相应的DOM对象。

```
var $txtName=$('#txtName');
var txtName=$txtName.get(0)
```
###jQuery选择器
####类似CSS选择器
1. 基本选择器
2. 层次选择器
3. 属性选择器

####过滤选择器
1. 基本过滤选择器
2. 可见性过滤选择器

>选择器书写很严格，多一个空格少一个空格都会影响选择器的效果。


###jQuery的样式设置

###直接设置样式
1. css(name,value)
###追加和删除样式
1. addclass(class)或addclass(class1....classN)
2. removeClass('style2')&remove("style1 style2")
###获取Value值
1. $(this).val()



##jQuery高级应用
###jQuery事件
1. window事件
2. 鼠标事件
3. 键盘事件
4. 表单事件
###事件注册语法
$(对象).type(fn)

###绑定事件
* bind()
* on()
>$(对象).on(type.[event],fn)
>
>可以为多个事件绑定方法

###移除事件
* unbind()
* off()
>$(对象).off([type],[fn])
>
>当不带参数时，表示移除所绑定的全部事件。

###委托事件
* delegate()方法用于委托事件的注册
> $(对象).delegate(子元素名，事件名，处理函数)
> 
>特点：
>利用事件冒泡机制实现委托
>提高事件处理的性能

###主动触发事件
1. trigger()
> $(对象).trigger(type)

###DOM
* jQery中的DOM操作可分为:
	* 内容及Value属性值操作
	* 节点操作
	* 节点属性操作
	* 节点遍历

####节点操作
* 查找节点
* 创建节点
* 插入节点
* 删除节点
* 替换节点
* 复制节点

> 替换节点用replaceWith
>
>复制节点用clone
>attr用来获取但是我们不用，我们用prop
>removeAttr()用来删除元素的属性

####遍历子元素
* $(body).children

####遍历同辈元素
1. next():紧邻元素之后
2. prev():紧邻元素之前
3. slibings():前后所有同辈元素
4. parent(),parents()：父级元素和祖先元素。


##jQuery动画

####显示及隐藏元素
1. show('速度')

####切换元素可见状态

1. toggle（）；
 
####淡入淡出效果
1. fadein():淡入
2. fadeout():淡出


####改变元素的高度
1. slideDown()
2. slideUp()


##jQuery-Ajax
###Ajax:异步刷新技术
####使用$.ajax()
	```
	$.ajax({
	url:url,
	type:'get',
	data:data,
	dataType:'text'
	success:function(result){
	},
	error:function(){
	}
	})
	```


