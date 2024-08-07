# 点此回到[[JAVA（由此开始）]]

## 字符串的本质是字符数组（字符序列），而equal比的是字符数组的每个位置的值
- 其中某个值为31，意思是二进制11111，能快速换位符计算

## String s1=null；   没有分配内存空间，容易报空指针异常
- String s1="";  分配了内存，但没有内容

## 不可变字符序列：String，（这里的不可变指字符串中，数组的引用不可变，即value【】不可变，value【】指向的堆地址不可变，，堆的值是可变的）
- String是特殊终结（finally）类，是个常量，不允许修改内容，值创建后不可改变，之所以之前重复赋值，其实是一直在开辟空间然后修改引用地址
- String直接赋值，是在常量池（方法区中），new 对象出来的是放在堆中，每new一个都会有不同地址，使用concat（）方法也是开辟新空间，除非用s1=s1.concat（“xx”）；覆盖原地址
- string实现了Comparable接口，可对字符串进行自然排序
- string类提供方法可以用于正则表达式


## 可变字符序列：（这两个的API都一样的，所以语法一致），一下修改都是修改本身，而不是新开辟内存空间
- StringBuffer，：
	- 是String的增强版，是字符串缓冲区，是个容器（默认为16（2的4次方）），一般拼接使用
		- 该类有关键字：synchronized，是保护线程安全的，意思是同步的，相当于加锁，但效率没有StringBulider高
		- StringBuffer(String str):有参构造 ，可以把一个String类型的数据构造成一个StringBuffer的对象，就可以调用 StringBuffer中的方法了
		- 常见方法
			- append():对字符串内容的拼接
			- delete():删除指定的内容
			- insert():在指定下标位置插入新的内容
			- reverse():反转字符内容
			- toString():把StringBuffer类型转换成String类型
- StringBulider：效率高，但不安全，容易产生死锁，

## String类在源码当中其实就是一个数组，在jdk1.8之前，是一个char类型的数组，在1.8之后，是一个byte类型的数组。
- 当数据量不多，并且对数据不会频繁的修改它的内容的时候，我们推荐使用String来进行数据的存储
- 修改String类中的内容，它并不是在原来内容的基础上进行修改的，每一次修改都会开辟新的内存空间

## 相关API
- length():可以获取字符串的长度，返回类型是int类型
- charAt(index):获取字符串对应下标的元素的值，返回的是一个字符类型的数据
- concat()：表示拼接内容，相当于“+”号拼接
- endWith():判断是否是指定的后缀结尾，返回boolean类型的结果
- startWith():判断是否以指定的前缀开头，返回boolean类型的结果
- equals(Object obj):比较字符串的内容是否相等，返回boolean类型结果
	- 如果是一般的类，当调用 equals方法的时候，有可能就是调用的Object中的equals方法，此时比较就是内存地址
	- String类它是已经重写了Object类中的equals方法的，它就可以比较当内存地址不同但是内容相同的情况
- equalsIgnoreCase()：忽略大小写的字母内容比较
- toLowerCase():把大写字母变成小写
- toUpperCase():把小写字母变成大写
- indexOf():**返回**指定字符在指定字符串中第一次出现的下标位置
	- 如果在字符串中没有找到，会返回一个-1，我们可以通过判断该方法返回的结果是否是-1来判断是否存在
	- 如果存在会返回它最后一次出现的下标位置
- lastIndexOf，返回最后出现的下标
- isEmpty():判断字符串长度是否为0，是否为空
- replace()：替换字符串中的内容
- split(    ，  ):可以把字符串内容按照指定的字符拆分成一个字符串类型的数组，返回的是一个字符串类型的数组
- subString():截取字符串中配合s1。indexOf("x")+1来指定的内容也可以subString( indexOf("x")   ，indexOf("x")+2 )；包括开头单不包括结束的下标
- trim():可以去掉字符串两边的空格

## 字符串常量池
- JVM创建一个新常量时会先在字符串常量池中检擦是否有这个字符串，如果有，就会**返回**池中的引用地址，如果创建的是对象，则复制改字符串在堆中复制为对象，


## String类特有的方法
- charAt(int index)    返回指定索引处的字符。
- codePointAt(int index)   返回指定索引处的字符的 Unicode 代码点
- codePointBefore(int index)    返回指定索引之前的字符的 Unicode 代码点
- compareTo(String anotherString)    按字典顺序比较两个字符串
- compareToIgnoreCase(String str)    按字典顺序比较两个字符串，不区分大小写
- concat(String str)   将指定字符串连接到此字符串的结尾
- contains(CharSequence s)    判断此字符串是否包含指定的字符序列
- endsWith(String suffix)    判断此字符串是否以指定的后缀结束
- equalsIgnoreCase(String anotherString)   将此字符串与另一个字符串进行比较，不区分大小写
- getBytes()    使用平台的默认字符集将此字符串编码为字节序列，并将结果存储到新的字节数组中
- indexOf(int ch)    返回指定字符第一次出现的索引
- replace(char oldChar, char newChar)
- replaceAll(String regex, String replacement
- split(String regex)
- startsWith(String prefix)
- substring(int beginIndex, int endIndex)   包前不包后
- toCharArray()    将此字符串转换为一个新的字符数组
- toLowerCase()    转小写
- toUpperCase()
- trim()  返回boolean参数的字符串表示形式
- valueOf(char c)   返回 `char` 参数的字符串表示形式
- valueOf(char【】 data)    返回字符数组参数的字符串表示形式
- valueOf(double d)
