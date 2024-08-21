# 点此回到[[JAVA（由此开始）]]

## 读取不同类型数据的方法
- 读取字符串
	- next(): 读取下一个标记（由空白字符分隔的字符串），忽略前导空白
	- nextLine(): 读取整行输入，包括空格和制表符
- 读取整数
	- nextInt(): 读取下一个整数。
- 读取浮点数
	- nextFloat(): 读取下一个浮点数（单精度）
	- nextDouble(): 读取下一个浮点数（双精度）
- 读取长整数
	- nextLong(): 读取下一个长整数。
- 读取布尔值
	- nextBoolean(): 读取下一个布尔值（true 或 false）
- 读取字节
	- nextByte(): 读取下一个字节值
- 读取短整数
	- nextShort(): 读取下一个短整数
- 获取某个字符
	- chat c1 =scn.next(),charAt(2);


## 检查输入可用性的方法
- 检查是否有下一个标记
	- hasNext(): 检查是否有任何类型的下一个标记。
- 检查是否有下一个整行输入
	- hasNextLine(): 检查是否有下一行输入
- 检查是否有下一个整数
	- hasNextInt(): 检查是否有下一个整数
- 检查是否有下一个浮点数
	- hasNextFloat(): 检查是否有下一个浮点数（单精度）
	- hasNextDouble(): 检查是否有下一个浮点数（双精度）
- 检查是否有下一个长整数
	- hasNextLong(): 检查是否有下一个长整数
- 检查是否有下一个布尔值
	- hasNextBoolean(): 检查是否有下一个布尔值
- 检查是否有下一个字节
	- hasNextByte(): 检查是否有下一个字节。
- 检查是否有下一个短整数
	- hasNextShort(): 检查是否有下一个短整数

## 特殊情况需要手动消耗回车键
- 先读取其他类型的数据，再读取一整行字符串，就需要手动消耗回车键，使用 nextInt()、nextDouble() 等方法后再调用 nextLine()时，需要手动消耗换行符以避免读取失败，手动调用一次nextLine()来消费掉这个换行符
- 使用 nextLine() 读取整行时，通常不需要额外处理换行符

## 要点：
- 例子：
	- String back = sc.nextLine();
	- int n1 = Integer.parseInt(back);
	- Integer.parseInt将一个表示整数的字符串转换为实际的整数值
- 此外还有：
	- double value = Double.parseDouble("123.45");
	- Byte.parseByte(String s)
-  Integer.parseInt与valueOf类似
	- Integer.parseInt返回的是基本数据类型
	- Integer.valueOf返回包装类型（如 Integer、Double）而不是基本数据类型
	- 用哪种类型取决于你的具体需求和代码上下文
		- 如果更关心性能并且只需要基本类型，那么 parse 方法是合适的
		- 需要包装类型的功能或需要将数值存储在集合中，那么 valueOf 方法会更合适