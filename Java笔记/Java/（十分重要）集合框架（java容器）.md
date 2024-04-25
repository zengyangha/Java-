# 点此回到[[JAVA（由此开始）]]

## java集合框架提供一套好的、方便的接口和类，位于java.until包中
## 这是面向接口编程，其特性是能自动扩展

## 有两大接口
- Collection（（接口）存放简单的API操作，单一一个值的，存着一组不唯一，无序的对象）
	- 特点：
		- 与数组不同的是可以存放不同数据类型，而数组只能放固定类型数据
		- 自动扩容
		- API具有（增、删、改）功能
	- List（接口）
		- （子类）存储着   不唯一，但有序（插入顺序）的对象
		- ArrayList
		- LinkedList
		- Stack(栈)
		- Vector
	- Set（接口）
		- （子类）存储着   唯一（元素不可重复），但无序的对象
		- HashSet
			- LinkedHashSet
		- TreeSet
- Map
	- HashMap
	- TreeMap

## 此外有个工具类名为：Collections，提供对集合进行排序，遍历等多种算法实现

