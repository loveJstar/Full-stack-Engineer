## 数组操作是否改变原数组

### 改变原数组

	shift：将第一个元素删除并且返回删除元素，空即为undefined
	
	unshift：向数组开头添加元素，并返回新的长度
	
	pop：删除最后一个并返回删除的元素
	
	push：向数组末尾添加元素，并返回新的长度
	
	reverse：颠倒数组顺序
	
	sort：对数组排序
	
	splice:splice(start,length,item)删，增，替换数组元素，返回被删除数组，无删除则不返回

### 不改变原数组的

	concat：连接多个数组，返回新的数组
	
	join：将数组中所有元素以参数作为分隔符放入一个字符
	
	slice：slice(start,end)，返回选定元素
	
	map,filter,forEach,some,every等不改变原数组

###splice和slice的区别： 

splice(i,j,”a”) 删除，添加元素，splice() 方法与 slice() 方法的作用是不同的，splice() 方法会直接对数组进行修改。从i开始删j个(包括i),并将”a”插入到i处。 

slice(start,end) 从某个已有的数组返回选定的元素，从start位开始返回到end（包括start不包括end）如果是负数，表示从数组尾部进行计算（同样：包括start不包括end）,请注意，该方法并不会修改数组，而是返回一个子数组。

--------------------- 
作者：cristina_song 
来源：CSDN 
原文：https://blog.csdn.net/cristina_song/article/details/77917404 
版权声明：本文为博主原创文章，转载请附上博文链接！