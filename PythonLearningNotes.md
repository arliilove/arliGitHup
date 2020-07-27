[Python学习网址](https://www.runoob.com/python3/python3-tutorial.html)
# Python3基本语法
## 编码
*   默认情况下，Python 3 源码文件以 UTF-8 编码，所有字符串都是 unicode 字符串。
## 标识符
*   第一个字符必须是字母表中字母或下划线 _ 。
*   标识符的其他的部分由字母、数字和下划线组成。
*   标识符对大小写敏感。
*   在 Python 3 中，可以用中文作为变量名，非 ASCII 标识符也是允许的
## 保留字/关键字/keywords
*   保留字即关键字，我们不能把它们用作任何标识符名称。Python 的标准库提供了一个 keyword 模块，可以输出当前版本的所有关键字：
```python
import keyword
keyword.kwlist
```
## 注释
*   Python中单行注释以 # 开头，实例如下：
```python
#第一个注释
print("Hello python") #第二个注释
```
*   多行注释可以使用多个#，或者'''或者"""，例如
```python
#第一个注释
#第二注释
'''
第三个注释
第四个注释
'''
"""
第五个注释
第六个注释
"""
print("Hello,python!")
```
## 行与缩进
*   **python最具特色的就是使用缩进来表示代码块，不需要使用大括号 {} 。**
*   缩进的空格数是可变的，但是同一个代码块的语句必须包含相同的缩进空格数。实例如下：
```python
if True:
    print ("True")
else:
    print ("False")
```
## 多行语句
*   Python通常是一行写完一条语句，但如果语句很长，我们可以使用反斜杠(\)来实现多行语句，例如：
```python
total = item_one + \
        item_two + \
        item_three
```
*   在 [], {}, 或 () 中的多行语句，不需要使用反斜杠(\)，例如：
```python
total = ['item_one', 'item_two', 'item_three',
        'item_four', 'item_five']
```
## 空行
*   函数之间或类的方法之间用空行分隔，表示一段新的代码的开始。
*   类和函数入口之间也用一行空行分隔，以突出函数入口的开始。
*   空行与代码缩进不同，空行并不是Python语法的一部分。书写时不插入空行，Python解释器运行也不会出错。但是空行的作用在于分隔两段不同功能或含义的代码，便于日后代码的维护或重构。
*   **记住：**空行也是代码的一部分。
## 等待用户输入
*   执行下面的程序就会等待用户输入，一旦用户按下回车键，程序就会退出
```python
myinput = input("请输入，按下enter键后退出")
print(myinput)
```
## 同一行键入多条语句
*   Python可以在同一行中使用多条语句，语句之间使用分号(;)分割，以下是一个简单的实例：
```python
import sys; x = 'runoob'; sys.stdout.write(x + '\n')
```
## 多个语句构成代码组
*   缩进相同的一组语句构成一个代码块，我们称之代码组
*   像if、while、def和class这样的复合语句，首行以关键字开始，以冒号( : )结束，该行之后的一行或多行代码构成代码组。我们将首行及后面的代码组称为一个子句(clause)。
*   如下实例：
```python
if expression : 
   suite
elif expression : 
   suite 
else : 
   suite
```
## Print输出
*   print 默认输出是换行的，如果要实现不换行需要在变量末尾加上 **end=""：**
```python
#!/usr/bin/python3
 
x="a"
y="b"
# 换行输出
print( x )
print( y )
 
print('---------')
# 不换行输出
print( x, end=" " )
print( y, end=" " )
print()
```
## import与from...import
* 在 python 用 **import** 或者 **from...import** 来导入相应的模块。
* 将整个模块（例如time）导入，格式为：```import time```，调用函数的格式为：```time.sleep(1)```
* 从某个模块（例如time）中导入所有函数，格式为：```from time import *```，调用函数的格式为：```sleep(1)```
* 从某个模块（例如time）中导入某个函数，格式为：```from time import sleep```，调用函数的格式为：```sleep(1)```
* 将模块（例如time）换个别名引入，格式为：```import time as abc```，调用函数的格式为：```abc.sleep(1)```
* 代码举例：
```python
#导入sys模块
import 

print('================Python import mode==========================')
print ('命令行参数为:')
for i in sys.argv:
    print (i)
print ('\n python 路径为',sys.path)
#导入sys模块的argv、path成员
from sys import argv,path

print('================python from import===================================')
print('path:',path) # 因为已经导入path成员，所以此处引用时不需要加sys.path
```
## help函数
* 调用 python 的 help() 函数可以打印输出一个函数的文档字符串：
```python
# 如下实例，查看内置函数 max 的参数列表和规范的文档
help(max)
```
# Python3基本数据类型
Python 中的变量不需要声明。每个变量在使用前都必须赋值，变量赋值以后该变量才会被创建。
在 Python 中，变量就是变量，它没有类型，我们所说的"类型"是变量所指的内存中对象的类型。
等号（=）用来给变量赋值。
等号（=）运算符左边是一个变量名,等号（=）运算符右边是存储在变量中的值。例如：
```python
#!/usr/bin/python3

counter = 100          # 整型变量
miles   = 1000.0       # 浮点型变量
name    = "runoob"     # 字符串

print (counter)
print (miles)
print (name)
```
## 多个变量赋值
Python允许你同时为多个变量赋值。例如：
```python
a = b = c = 1
```
以上实例，创建一个整型对象，值为 1，从后向前赋值，三个变量被赋予相同的数值。
您也可以为多个对象指定多个变量。例如：
```python
a, b, c = 1, 2, "runoob"
```
以上实例，两个整型对象 1 和 2 分配给变量 a 和 b，字符串对象 "runoob" 分配给变量 c。
*   *   *   
## 标准数据类型
Python3 中有六个标准的数据类型：
* Number(数字)
* String(字符串)
* List(列表)
* Tuple(元组)
* Set(集合)
* Dictionary(字典)
Python3 的六个标准数据类型中：
* **不可变数据(3个)：**Number（数字）、String（字符串）、Tuple（元组）；
* **可变数据(3个)：**List（列表）、Dictionary（字典）、Set（集合）。
*   *   *   
## Number(数字)
Python3 支持 **int、float、bool、complex（复数）**。
在Python 3里，只有一种整数类型 int，表示为长整型，没有 python2 中的 Long。
像大多数语言一样，数值类型的赋值和计算都是很直观的。
内置的 type() 函数可以用来查询变量所指的对象类型。
```python
a, b, c, d = 20, 5.5, True, 4+3j
print(type(a), type(b), type(c), type(d))
```
此外还可以用 isinstance 来判断：
```python
a = 111
print(isinstance(a,int))
```
isinstance 和 type 的区别在于：
* type()不会认为子类是一种父类类型。
* isinstance()会认为子类是一种父类类型。
*   *   *   
***注意：**在 Python2 中是没有布尔型的，它用数字 0 表示 False，用 1 表示 True。到 Python3 中，把 True 和 False 定义成关键字了，但它们的值还是 1 和 0，它们可以和数字相加。*
*   *   *   
当你指定一个值时，Number 对象就会被创建：
```python
var1 = 1
var2 = 10
```
您可以使用del语句删除一些对象引用，也可以通过使用del语句删除单个或多个对象。例如：
```python
del var1
del var_a,var_b
```
**注意**：
1. Python可以同时为多个变量赋值，如a, b = 1, 2。
2. 一个变量可以通过赋值指向不同类型的对象。
3. 数值的除法包含两个运算符：/ 返回一个浮点数，// 返回一个整数。
4. 在混合计算时，Python会把整型转换成为浮点数。
**数字类型实例**
| int | float | complex |
| :-: | :---: | :-----: |
| 10  | 0.0   | 3.14j   |