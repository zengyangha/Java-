# 点此回到[[JavaScript/开头]]

## JavaScript让网页具有交互功能，让浏览器去解析脚本运行

## 特性：
- 基于对象，但不完全面向对象
- 解释型语言，不编译或者生成中间产物，直接在浏览器中运行
- 弱类型语言，格式要求不严格

## 组成：
- ECMA Script，脚本语言规范，是JavaScript的核心语法基础
- BOM，Browser Object Model 浏览器对象模型，操作浏览器中各种对象
- DOM，Document Obeject Model文档对象模型，操作网页中标签元素

## 五种数据类型
- number
- boolean
- string
- object
- undefined

## null是对象类型，只是对象没有值

## 转换
- parselnt，将字符串类型的数字转换成整数类型
- parseFloat，转换浮点类型
- isNaN，字符流类型转换，非数字返回true，是数字返回flase，意思是is not a number

## 在if判断中，
- number   1为真，0为假
- string中，非空为真，空为假，""
- undefined为假
- NaN为假
- object中非空为真，null为假

## window对象方法，其中window可以省略
- prompt("提示词" ，"默认值")，弹框写值
- alert， 弹窗警告
- confirm，弹窗确认

## 函数使用，函数都有隐藏的数组，arguments
- 命名函数
	- function sum(  ){  代码块    }
- 匿名函数
	- var sum=function(a,b){     }


## 输出常用方法，
- concat（），拼接，返回评好的数组
- reverse（），反转数组
- join（），拼接
- sort（），排序


## 会话
- 会话是浏览器与服务器之间的一次通讯过程
- application和ServletContext作用相同，上下文，
- session 会话，访问服务器就会创建一个会话，在服务器内存中独有空间，客户端只有一个唯一标记凭证
- pageContext，当前页的域对象，存储的数据只能当前jsp页面访问
- 





