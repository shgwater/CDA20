
# Python语法

安装新的包
管理员权限打开cmd
输入命令>>>conda install chardet
既可以安装chardet包。

## 第二章Python基础语法

### 标识符
- 第一个字符必须是字母表中的字母或者下划线
- 大小写敏感。
- 其它组成部分为字母数字下划线

### 等号：
“=”含义为赋值，用来定义变量

### Python保留字
``` python
import keyword
print(keyword.kwlist)
```

### 注释：
# 或 （``` code ```)

### 行与缩进
可用分号进行分割，但是推荐用行进行分割。

### 输入和输出：
Python提供了一个input()，可以让用户输入字符串，并存放到一个变量中。 ，
print()在括号中加上字符串，就可以向屏幕上输出指定文字。

### 变量

- Python中的变量处需要声明。每个变量在使用前都必须赋值，变量赋值之后该变量才会被创建。
- 在Python中个，变量就是变量，它没有类型，我们所说的类型是变量内存中对象的类型。
- 使用（=）进行赋值。



#### 自增运算

e.g. >>> a = a+1
or >>> a+=1

|运算符| 描述 | 实例 |
| --- | --- |--- |
| = | 简单的赋值运算符 | c= a+b 将a+b的结果赋值为c |
| += | 加法赋值运算 |b += a 等价于 b = b+a |
| -= | 减法赋值运算 | b -= a 等价于b = b-a |
| x= | 乘法赋值运算符 | b x= 等价于 b= bxa|
| /= | 除法赋值运算 | b /= a 等价于 b=b/a |
| %= | 取模赋值预算 | b=b%a |
|xx=|幂赋值运算||
 | //= | 取整除赋值运算符 | |
 

#### 多个变量赋值
``` python
a = b= c=1
e,f,g=1,2,"runoob"
#星号表示不定长，例如
a,*b,c=1,2,3,4,5
#此时b为一个列表
```

#### 分支主题

## 第三章 标准数据类型

使用 type(a)来查看变量类型。
使用isinstance(3,int)查看3是否为整数，返回布尔值。

- 布尔值 True 和 False,其中0和空序列 为True

### 1.布尔值 booleans

#### 布尔运算（and,or,not)

### 2.数字Numbers

#### 整数int

#### 小数float

注意，可以用int函数或者整除来将小数型的数据经过运算转化为整型数据。

第一个不同。
小数在Python中是不精确存储，可以使用包import decimal来解决。
e.g.
decimal.Decimal("1.1")+decimal.Decimal("1.1")+decimal.Decimal("1.1")
此时为精确计算。

第二个不同。
整数存储赋值，使用id()查看对象的内存存储位置。当整数小于256时，python内部有，可以直接调用。但是浮点类型是不精确存储的，每次新建都是重新创建对象。


#### 数字间的转换。

#### 比较运算符与布尔运算？

### 3.字符串Strings

字符串是以单引号'或双引号"括起来的任意文本。
字符串不可修改。
字符串位置是从0开始的。

#### 切片函数:[]

String_1[x:y:z]
- x起始位置
- y终止位置
- 步长
- 起始位置包含起始位置的索引，终止位置不包括终止位置的索引。
- 步长默认为1.

e.g.
str_1[::2]
步长为2.

#### 字符串运算符

##### "python"+"python"
"python""ssss"

##### "python"*3

#### 转义字符 "\"

##### \n 
换行

##### \t
表示制表符,tab键，相当于四个空格。

##### \\
表示 \，只在字符串中有效。

##### r''或者R''
用r''表示''内字符串默认不转义，也就是使用原生字符串。

#### 多行字符串

三双引号是用来多行注释的，但是换行符会用 \n 来表示。
e.g.
``` python

"""
a 是一个数字
b 是一个字符串
c 是一个列表
"""

```
返回
``` python
'\na 是一个数字\nb 是一个字符串\nc 是一个列表\n'
```



#### 常用字符串方法

字符串练习
练习1.1：
已知字符串 s = “sadINDUionaREwSS” ，能否将该字符串前半部分转换大写，后半部分转换成小写？为什么？（若字符串长度为奇数，中间的字符大写。）
``` python
s = "sadINDUionaREwSS"
s[0:int(len(s)/2)].upper()+s[int(len(s)/2):].lower()
```
练习1.2：
请生成字符串s3，s3为s进行逆序排序的结果。
``` python
for i in range(15):
    s3=s3+s[15-i]
    
s3=s[::-1]
```
练习1.3：
请基于练习一中的截取s中奇数位并转化为大写，截取s中偶数位并转换为小写。
``` python
for i in range(int(len(s))):
    if i % 2 == 0:
        s1_3=s1_3+s[i].lower()
    else:
        s1_3=s1_3+s[i].upper()
    print(s1_3)
    
    
s[::2].upper()
s[1::2].lower()
```
练习1.4：
"2017/10/15 14:15:45"这个时间的字符串，请截取年份，月份，日期，时，分，秒
``` python
time.split("/")[0]
time.split("/")[1]
time.split("/")[2].split(" ")[0]
time.split("/")[2].split(" ")[1].split(":")[0]
```
练习1.5：
用input输入一个数字的字符串，然后转换成整型，然后乘以5加上8计算后转换成字符串输出
``` python
str(int(a)*5+8)
```
练习1.6：
str10="aabbccddeeabbbadddd"将用A将前2个a替换，然后用find函数返回最后一个a的索引
``` python
str10.rfind["a"]
```

##### 大小写
string.upper()
string.lower()

##### 替换
string.replace("y","Y",2); 2表示一共替换几个。

##### 切分函数
string.split('t')#一个参数，参数为分隔符。如果没有的话，默认使用空格进行切分。

##### 拼接方法
"th".join(['py','on py','on']);使用th把序列中的元素拼接到一起。如果后面是一个字符串，则在字符串的每个单元之间拼接th。

##### 计数
string.count("y")

##### 去掉空格
string.strip();string.lstrip();string.rstrip()

##### 查找字母位置
string.find("y",4,7)在4到7的位置上找y。

##### 格式化字符串
注意，format前面为“点”不是“逗号”
for i in range(4):
	print("i的值为{}，i的平方为{}，i的立方为{}".format(i,i**2,i**3))

##### in
"a" in str_2;判断a是否在字符串中，返回值为布尔值。

### 4. 列表
列表就是用来存储一连串元素的有序的容器，用[]来表示。

``` python 
L=[1,2,3,4,"str"]

L[0]=78
```
与字符串有重要区别，列表是可以修改的。
赋值不需要位数相等，但是需要值也为列表形式。**赋值需要前后类型相同。但是个数不一定相同。**
``` python 
L[1:3]=[45]  #成功
L[1:3]=45  #失败，需要前后的类型相同。

```

#### 常用方法

练习1.7：
列表L，[2,5,3,8,10,1],对其进行升序排序并输出
``` python
L=[2,5,3,8,10,1]
L.sort(reverse=False)
L
```

练习1.8：
字符串s，"123456"，将其转化成列表逆序并输出
``` python
S=list(s)
S.reverse()
S
```
练习1.9：
l=[1,2,3]有几种方法可以扩展成[1,2,3,4,5,6]
``` python
L.extend([4,5,6])
L+[4,5,6]
```

练习1.10：
List=[1,3,5,7,9,0,2,4,6,8]使用切片得到[4, 0, 7]，[5, 9, 2, 6]
``` python
List[7:2:-2]
List[2::2
```

##### 添加元素
L.append("x");不管x是什么对象类型，只能添加成原有列表中的一个元素。

##### 减少元素
L.pop()

删除列表中最后一个元素，然后返回这个元素。


##### 插入元素
L.insert(1,"python");将“python”这个字符串插到索引为1的位置

##### 拼接列表
L.extend([5,6,7]);吧[5,6,7]和L进行拼接，与append相比，会将列表连接在原列表后。

##### 列表运算
加法为拼接，乘法为复制n次

##### 计数
L.count(4)

##### 索引切片
L[-1][1]

##### 移除元素
L.remove(45)，参数为列表里面的值

##### 逆序/降序
L.reverse()与L[::-1]不同。

##### 排序
需要列表内元素是同质的，或者有一定规则可以排序。

``` python
L=[1,3,2,7,3]
L.sort()
L1=["aaabbd","ccccddddd","ffsas"]
L1.sort(key=len) #按照长度排序
L1.sort(key=len,reverse=Ture) #降序排列

```

##### 清空
L.clear()

##### list()
将字符串转化为列表

### 5.元组
与列表相似，但是不能修改。常用(34,55,66)表示。但是如果元组之中有列表的话，可以修改其中的列表。
可以这样理解，列表是一种容器，如果新建一个列表L=[1,2,3]然后查看它在内存中的位置id(L).然后向列表中添加元素L.append(4)，此时查看id(L)，会发现两个id相同，说明L没有变。

``` python
a= 4,5,6
a,b,c = 4,5,6

```

### 6.字典Dictionaries
字典使用 键-值（key-value）存储，具有极快的查找输入速度，也需要大量内存。
字典的每个key-value对用冒号分割。
字典中的每个 键key 是唯一的、不可变的，但是 值value 可以重复。 

dca={'Atom':25,'BIG':35,'Kid':40}

字典练习
练习1.11:
建一个字典，添加新的键值对，在此基础上更新另外一个字典，在将字典以列表的方式返回。
``` python
dict_1 = {"a":1,"b":2,"c":3}
type(dict_1)
dict_1["e"]=5
dict_1.update({"d":4})
list(dict_1.items())
```
练习1.12：
Dict={"d":"banana","a":"apple","b":"grape","c":"orange"}转换成列表用键进行排序。
``` python
l=list(Dict.items())
l.sort()
l
```
练习1.13：
d={"a":1,"b":2,"c":3},分别输出它的key与value。向其插入字典{"d":4}
``` python
d.keys()
d.values()
d_1={"d":4}
d.update(d_1)
d
```

#### 常用操作

##### 创建字典
dca={'Atom':25,'BIG':35,'Kid':40}

##### 新增键值对
dca["lucy"]=98

##### 修改键值对
dca["lucy"]=80

##### 查询键值对
dca["lucy''];根据键来找值。

##### 删除键值对
del dca["lucy"]

#### 常用方法

##### 删除键值对
dca.pop("lily","No Such Key")
好处是不太容易删错

##### 增加键值对
dca.update({"a":2,"c":5})

##### 转化为列表
list(dca.item())

##### 校验增加
如果dca中存在BIG，则返回字典中BIG的值，如果没有的话，将BIG插入到dca中。
dca.setdefault("BIG",11)

##### 返回键/值
dca.keys()
dca.value()

### 7.集合
set和idct类似，为一组key的集合，但不存储value。由于key不能重复，所以在set中不能有重复的值。
是无序的。

### 8.空值
None，Python中的特殊值。

## 第四章 控制流语句

**使用缩进来控制语句层级**同缩进的代码被认为是同等级的代码。 

练习1.16：
打印出所有的“水仙花数”，所谓“水仙花数”是指一个三位数，其各位数字立方和
``` python
I=[]
for i in range(100,1000):
    i=str(i)
    if int(i)==int(i[0])**3+int(i[1])**3+int(i[2])**3:
        
        I+=[int(i)]
print(I)
```
练习1.17：
有四个数字：1、2、3、4，能组成多少个互不相同且无重复数字的三位数？各是多少？
``` python 
I=[]
for i in range(1,5):
    for j in range(1,5):
        for k in range(1,5):
            #if i!=j!=k:
            if i!=j and j!=k and i!=k:
                I+=[int(str(i)+str(j)+str(k))]
len(I)
```
练习1.24:
**华为2016校招（字符集合）**
题目描述
输入一个字符串，求出该字符串包含的字符集合
输出描述:
每组数据一行，按字符串原有的字符顺序，输出字符集合，即重复出现并靠后的字母不输出。 输入例子:
abcqweracb
输出例子:
abcqwer
``` python
S=input("请输入一串字母：")
S_1=S[0]
for i in range(0,len(S)):
    if S[i] in S_1:
        S_1=S_1
        #continue
    else:
        S_1+=S[i]
print(S_1)

#第二种方法
"".join(sorted(set(S_1),key=S_1.find))
#先化为集合，因为集合的性质是不能有重复值，但是集合是无序的。
#所以需要使用sorted()函数进行排序，是一个高级函数。
#排序的依据是原字符串的索引。key=S_1.find 或者 key=S_1.index
#最后使用字符串的join方法将这些单独的字符串连接起来。
```


### 第一节 顺序结构
就是普通的从上到下的代码结构。
顺序结构，自上而下逐条运行

### 第二节 分支结构
Python条件语句是通过一条或多条语句的执行结果（True或False）来决定执行的代码块。

``` python
#条件判断要求其为布尔值。
if<条件判断1>:
	<执行语句块1>
elif<条件判断2>:
	<执行语句块2>
else:
	<执行语句块3>
    
age = input("Enter Your Age:")

if int(age) > 60:
    print("old man")
elif int(age) > 28:
    print("adult")
else:
    print("child")
```
企业发放的奖金根据利润提成。利润(I)低于或等于10万元时，奖金可提10%；利润高于10万元，低于20万元时，低于10万元的部分按10%提成，高于10万元的部分，可提成7.5%；20万到40万之间时，高于20万元的部分，可提成5%；40万到60万之间时高于40万元的部分，可提成3%；60万到100万之间时，高于60万元的部分，可提成1.5%，高于100万元时，超过100万元的部分按1%提成，从键盘输入当月利润I，求应发放奖金总数？
``` python
I=input("请输入当月利润（单位：万元）：")
if int(I)<=10:
    print(int(I)*0.1,"万元")
elif int(I) <= 20:
    print(10*0.1+(int(I)-10)*0.075,"万元")
elif int(I) <= 40:
    print(1.75+(int(I)-20)*0.05,"万元")
elif int(I) <= 60:
    print(2.75+(int(I)-40)*0.03,"万元")
elif int(I) <= 100:
    print(3.35+(int(I)-60)*0.015,"万元")
else:
    print(3.95+(int(I)-100)*0.01,"万元")
    
I=int(input("enter the price"))#可以在输入的时候就将其变为整型

#第二种方法
dollar = int(input("please enter profit:"))
profit = [100,60,40,20,10,0]
i = [0.01,0.015,0.03,0.05,0.075,0.1]
money = 0
for index in range(len(i)):
    if dollar>profit[index]:
        money+=(dollar-profit[index])*i[index]
        dollar=profit[index]
print(money)
    
```

### 第三节 循环结构
用来控制一段语句的重复执行。
**Python循环语句**
- Python中的循环语句有for和while。
- Python中通过条件判断来确定是否执行循环体。

#### while循环

``` python
while <条件判断>:
	<执行语句块1>
    #完成后再次返回while
else:
	<执行语句块2>#else在条件语句为false时执行else语句块
#else部分可以省略

#对列表进行循环判断
L = [4,6,7,8,10]
flag = 1
index = 0
while flag:
    if L[index]%2 == 0:
        print(L[index])
    else:
        flag = 0
    index = index+1
else:
    print("奇数的位置索引：",index-1)
#使用变量来控制while循环的停止，这样就不用使用break进行跳出了。
#使用index对列表中的对象使用切片器进行索引。
```

#### for循环
经常搭配range(1,10,2)使用，1为起始值，10为终止值，2为步长。只填一个数默认为终止值。函数默认从0开始计数。

``` python
for i in <可迭代对象>:
	<执行该语句块1>
else:
	<执行语句块2>#else中的语句会在循环正常执行完（即for不是通过break跳出而中断的）的情况下执行。
    
```
可迭代对象常用列表，元组也是可迭代对象。
``` python
for i in L[1,2,3,4]:
	print(i)#i相当于每次从L中取一个元素。
```
九九乘法表
``` python
for i in range(1,10):
    for j in range(1,10):
        if i>=j:
            print(i,"*",j,"=",i*j,end="")
    print()
```
字典中的值如何通过循环取出来。**重点在于，for后边的变量与in后面的对象的格式要相对应**
``` python
dict_1={"a":1,"b":2,"c":3}
dict_1
for i,j in dict_1.items():
    print("i={},j={}".format(i,j))

L=[(1,2,3),[4,5,6]]
#此时 * 表示不定量，j的结果为一个列表
for i,*j in L:
    print("i={},j={}".format(i,j))
```
 输入一个数字，输出它的二进制中的1的个数
 ``` python
 num = bin(int(input("please enter number:")))
count=0
for i in num[2:]:
    if i=="1":
        count=count+1
print("这个数字的二进制中包含1的个数为:{}".format(count))

#第二种方法
two=bin(int(input("aaa")))
two.count("1")
print(two,two.count("1"))

#求二进制中连续出现1最多的次数
len(max(bin(442)[2:].split("0"),key=len))
 ```
 
 
 
 


#### 终止语句
break语法用来终止最内层的循环

``` python
n = 6
while 1:
	if n%2 == 0:
    	print(n)
    else:
    	print(n**2)
    n-=1
    if n == 0:
    	break
```


#### continue
continue用来跳过最内层当前次的循环

#### pass占位语句
pass是空语句，是为了保持程序结构的完整性。

## 第五章 自定义函数

解一元二次方程
``` python
def solve_quar(a,b=0,c=0):
    if a==0:
        print("请输入正确的参数")
        return()
    elif b**2-4*a*c < 0:
        print("没有实数解")
    else:
        print("结果如下")
    return((-b+(b**2-4*a*c)**0.5)/(2*a),(-b-(b**2-4*a*c)**0.5)/(2*a))
```
老师解法
``` python
def slove(a,b,c):
    if a==0:
        print("不是一元二次")
    else:
        x=-b/(2*a)
        delta=b**2-4*a*c
        if delta==0:
            print("只有一个根")
            return x
        elif delta>0:
            x1=x-math.sqrt(delta)/(2*a)
            x2=x+math.sqrt(delta)/(2*a)
            print("有2个根x1={}，x2={}".format(x1,x2))
            return(x)
        else:
            print("不考虑")
```

求欧式距离
``` python
#两变量的欧式距离
##两个位置的参数使用列表
def oushi(a,b):
    return math.sqrt((a[0]-b[0])**2+(a[1]-b[1])**2)

oushi([1,2],[3,4])

def oushi(a,b):
    dis = 0
    for i in range(len(a)):
        dis+=(a[i]-b[i])**2
    distance = math.sqrt(dis)
    return distance
    
oushi([1,2,3,4],[4,3,2,1])
```
    
曼哈顿距离
``` python
def manha(a,b):
    return sum(map(lambda x,y:abs(x-y),a,b))
manha([2,3],[4,5])
```

### 第一节 自定义函数的结构

自定义函数
其中，map函数规则为：map() 会根据提供的函数对指定序列做映射。第一个参数 function 以参数序列中的每一个元素调用 function 函数，返回包含每次function 函数返回值的新列表。
map(function, iterable, ...)

lambda为匿名函数，适用于只有一个条件的简短函数，可直接用于条件。
lambda x:x+=1
``` python
def func(n):#func为函数名，n 为参数
    """用来求n位的水仙花数"""
    x = 10**(n-1)
    y = 10**n
    res = []
    for i in range(x,y):
        if sum(map(lambda x:int(x)**n,str(i)))==i:
            res.append(i)
    return res#返回变量，并且终止函数 
```
调用函数
``` python
func(3)
```

### 第二节 函数的参数

	

#### 必须参数

必须参数又称为位置参数，必须以正确的顺序传入参数。调用时的数量和位置必须和声明时的一样。
``` python
def func1(x,y):
	return x**y
```

#### 命名参数

给定参数一个默认值，按照顺序来，如下例，当只输入一个参数的时候，默认y为2，也可以输入两个参数，自定义y的值。
``` python
def func1(x,y=2):
	return x**y
```
输入参数的时候也可以带上参数的名称，这样可以不按照顺序来。
func1(y=4,x=2)

#### 默认参数

### 第三节 return语句

return [表达式]语句用于退出函数，选择性地向调用方式返回一个表达式，不带参数的return语句返回None

### 第四节 变量作用域

局部内不能修改全局的变量。**注意，像列表之类的容器，可以使用list.append对容器内的内容进行修改！**
可以使用 global 可在局部中指定一个全局的变量，并且进行修改。
``` python
a = 10
def fff():
    global a 
    a=4 
    print(a)
```

``` python
x = int(2.9)#内建作用域

g_count = 0 # 全局作用域
def outer():
    o_count = 1 #闭包函数外的函数中
    def inner():
        i_count = 2 #局部作用域
        print(i_count)
        print(o_count)
        print(g_count)
    inner()
outer()
```

### 第五届 递归函数

``` python
def func(n):
	if n==1:
    	return 1
    else:
    	return func(n-1)*n
```

### 第六节 匿名函数

lambda表示匿名函数，与自定义函数相比不占用内存，用完就可以丢掉了。
func = lambda x:x+x
func(1)
冒号前面表示函数参数。匿名函数有个限制，**就是只能有一个表达式**，不用写return，返回值就是该表达式的结果。用匿名函数有个好处，因为函数没有名字，不必担心函数名冲突。
**匿名函数也是一个函数对象，可以把匿名函数赋值给一个变量，再利用变量来调用该函数。**


### 高级函数

练习1.36:
hh=[11,22,33],在每个元素上加100(分别用def和lambda) [11,22,33],[44,55,66],[77,88,99]想得到[114477,225588,336699] (分别用def和lambda)
``` python
hh=[11,22,33]
list(map(lambda x:x+100,hh))

def plus100(x):
    return x+100
list(map(plus100,hh))
#拼接三个序列
a,b,c=[11,22,33],[44,55,66],[77,88,99]
list(map(lambda x:int(str(a[x])+str(b[x])+str(c[x])),[0,1,2]))

def plus(x):
    return int(str(a[x])+str(b[x])+str(c[x]))
list(map(plus,[0,1,2]))
```
练习1.37:
a=list(range(1,10)) b=list(range(2,20,2))#求a+b，对应的元素相加
``` python 


```
练习1.37:
a=list(range(1,10)) b=list(range(2,20,2))#求a+b，对应的元素相加


#### map

对序列使用的函数，类似于循环，遍历里面的所有元素。
``` python
list(map(lambda x:x>0,[1,2,3,4,-6]))
[True, True, True, True, False]

filter
list(filter(lambda x:x>0,[1,2,3,4,-6]))
[1, 2, 3, 4]
```

#### reduce

把一个函数作用在序列上。

#### filter

filter函数用来过滤，第一个参数为判断函数，返回布尔值，以此来**过滤**第二个参数（序列）中为TRUE的对象。

``` python
def is_odd(x):
    """删掉偶数只保留奇数"""
    return x%2==1 #返回的是布尔值
list(filter(is_odd,[1,2,3,4,5,6]))
#或者使用匿名函数
list(filter(lambda x:x%2==1,[1,2,3,4,5,6]))
```

#### zip函数

``` puthon
L=list(zip(["A","B","C"],[1,2,3,4],["d","e","f"]))
#out:[('A', 1, 'd'), ('B', 2, 'e'), ('C', 3, 'f')]
#返回，也就是说将元组打碎,将对应位置的值放在一起。
list(zip(*L))
#[('A', 'B', 'C'), (1, 2, 3), ('d', 'e', 'f')]
```

#### 自定义排序
sorted([43,2,-12,4,-24],key=abs)

key比较灵活，例如
- key=lambda x:x[1]
- key=lambda x:len(x[2])

还有一个参数 reverse=True 也就是按照倒叙排序

#### 棋盘问题

``` python
#棋盘问题
L=[]
n=int(input("请输入n的值："))
for i in range(n):
    L.append(input("输入你的棋盘颜色："))

max_b=max(map(lambda x:max(x.split("W")),L))#在行中通过W切分的最大的长度。
max_w=max(map(lambda x:max(x.split("B")),L))#在行中通过W切分的最大的长度。

#使用zip进行转置，看一下列的相邻的数量
list(zip(*L))
list(map(lambda x:"".join(x),(zip(*L))))


max_arry_b=max(map(lambda x:max(x.split("W")),L))#在列中通过W切分的最大的长度。
max_arry_w=max(map(lambda x:max(x.split("B")),L))#在列中通过W切分的最大的长度。

len(max(max_b,max_w,max_arry_b,max_arry_w,key=len))
```

#### 列表生成式

``` python
[i if i%2==0 else -i for i in range(10) ]
#相当于
L=[]
for i in range(10):
    if i%2==0:
        L.append(i)
    else:
        L.append(-i)
L
```
三元表达式
简便写法的时候if else要放在前面，因为是一个三元表达式。
``` python
10 if 4>0 else 3
```
从matrix中取出每个列表中的顺序个重新生成新的列表(列表生成器)
``` python

matrix=[[1,2,3,4],[5,6,7,8],[9,10,11,12]]
[[l[i] for l in matrix] for i in range(4)]

#生成一个列表
[l[i] for l in matrix for i in range(4)]
[j for i in matrix for j in i]
```

##### 练习

练习1.40:
strings=["a","as","bat","car","dove","python"]过滤掉长度小于等于2的字符串，并将剩下的字符串转换成大写字母形式。
``` python
strings=["a","as","bat","car","dove","python"]
list(filter(lambda x:len(x)>2,list(map(lambda x:strings[x].upper(),range(len(strings))))))
#第二种
[x.upper() for x in list(filter(lambda x:len(x)>2,strings))]

```
练习1.41：
strings=["a","as","bat","car","dove","python"]创建一个指向列表位置的映射关系的字典。
``` python
strings=["a","as","bat","car","dove","python"]
{i:j for j,i in enumerate(strings)}

#two
dict(enumerate(strings))
```
练习1.42:
some_tuples=[(1,2,3),(4,5,6),(7,8,9)]将这个整数元组构成的列表成为一个简单的整数列表。
``` python
some_tuples=[(1,2,3),(4,5,6),(7,8,9)]
[j for i in some_tuples for j in i]
```
练习1.43:
all_data=[["Tom","Billy","Jefferson","Andrew","Wesley","Steven","Joe"], ["Susie","Casey","Jill","Ana","Eva","Jennifer","Stephanie"]]我们要找出带有2个或以上的字母e的名字，并将它们放入一个新列表。
``` python
all_data=[["Tom","Billy","Jefferson","Andrew","Wesley","Steven","Joe"], ["Susie","Casey","Jill","Ana","Eva","Jennifer","Stephanie"]]
"ee".count("e")
[j for i in all_data for j in i if (j.count("E")+j.count("e"))>=2 ]

```

#### 字典生成式

``` python
L=["a","b","c","d"]
{i:j for j,i in enumerate(L)}
#list(enumerate(L))
```

## 第六章 错误和异常

### 异常

有很多，参考
http://www.runoob.com/python/python-exceptions.html


#### 1. 语法错误

sy

#### 2. 除0错误 ZeroDivisionError

ZeroDivisionError

#### 3. 访问一个错误的方法 AttributeError

#### 4. 索引的值超过索引的范围 IndexError

#### 5. 字典的键错误 KeyError

#### 6. 变量名错误 NameError

#### 7. I/O错误

#### 8. 类型产生的错误 TypeError

### 异常处理

- 用来捕获程序中出现的异常，用来保证程序的正常运行。
``` python
try
	<执行语句块0>
except <异常信息1>:
	<执行语句块1>#如果在try部分引发了异常1
except<异常信息2>:
	<执行语句块2>#如果在try部分引发了异常2
else:
	<执行语句块3>#如果在try部分没有引发异常
finally：
	<执行语句块4>#无论发生什么异常都执行，一般用于打开文件最后关闭文件。还有连接数据库最后关闭数据库连接
```

- 注：如果except后不写异常的类型信息，那么该except会捕获所有的异常。
- 如果一个except捕获多个异常那么异常信息的位置传入包含多个异常的元组即可

e.g.
``` python
L=[] 
for i in range(4):
    try: 
        a = int(input()) 
        L.append(a) 
    except ValueError as e:  
        print("出现了异常，错误信息为{}".format(e)) 
        continue
    else:
        print("没出现错误")
    finally:
        print("一定会执行")
```

#### 猜数字问题

<!--Note-->
###### 异常处理习题
- 猜数字问题
- 训练内容: 分支结构, 循环结构, 异常处理
- 问题描述: 由系统程序产生一个 1 - 100 之间的随机整数, 然后去猜测数字是多少, 猜测正确或者猜测次数超过5次, 给出相应提示并结束游戏.
``` python
import random
count=0
guess = random.randint(1,100)
while True:
    try:
        count+=1
        a = int(input("please enter a number:"))
    except ValueError as e:
        print("please enter a number,Error is :")
        continue
    if a > guess :
        print("猜大了")
    elif a< guess:
        print("猜小了")
    else:
        print("猜对了，数字为{}".format(a))
        break
    if count == 5:
        print("guess={}".format(guess))
        break
```
<!--/Note-->

#### 蒙特卡洛模拟计算π
画图

总的思想就是根据四分之一圆外切正方形的面积比来计算π。也就试根据圆的面积S=πr^2得到
``` python
tik = time.time()
count=0
cycle=2**20
x_inp=[]
y_inp=[]
x_out=[]
y_out=[]
#循环
for i in range(cycle):
    #生成一个随机点
    x,y=random.random(),random.random()
    #判断是否在圆内
    if x**2+y**2<1:
        count+=1
        x_inp.append(x)
        y_inp.append(y)
    else:
        x_out.append(x)
        y_out.append(y)
tok= time.time()
pi = 4*count/cycle
print(pi)
print(tok-tik)
```
画图
``` python
import matplotlib.pyplot as plt#画图的包，as后面是别名，方便调用
%matplotlib inline#实时展现
plt.figure(figsize=(8,8))
plt.scatter(x=x_inp,y=y_inp)
plt.scatter(x=x_out,y=y_out,color="r")
```

## 第七章 常用内置函数

### 第一节 逻辑判断

#### all(iterable)
如果iterable中值都为真，返回ture，如果iterable为空也返回Ture。

#### amy(iterable)
有任意一个值为真，返回Ture，如果iterable为空返回False

#### isinstance()
判断参数是否为指定类类型

``` python
isinstance(2,int)
```

### 第二节 数学相关

#### abs(x)
绝对值

#### divmod(x,y)
完成除法，返回商和玉树

#### pow(x,y[,z])
pow()函数返回以x为底，y为指数的幂。如果给出z值，该函数就计算x的y次幂被z取模的值。

#### round(x,[,n])
round()函数返回浮点数x的四舍五入值，如给出n值，则代表舍入到小数点后的位数。

#### min(x,[,y,z...]
min()函数返回给定参数的最小值，参数可以为序列

#### max(x,[,y,z...])

#### sum(iterable)
返回序列或集合中数字的综合

### 第三节 序列相关

#### len(object)->integer

#### range([lower,]stop[,step])

### 第四节 类型转换

#### bool()

#### int()

#### float()

#### str()

#### dict(iterable)

#### list(iterable)

#### tuple(iterable)元组

#### set(iterable)
创建一个无序不重复元素的集合

#### complex（）
复数

#### enumerate()
将字符串或序列生成序列对应元组

### 第五届 系统函数

#### id()

#### help()

#### type()

#### input()

#### open()

#### print()

#### eval()

将字符串作为代码运行，较多与input结合


## 第八章 模块

a

### 自定义模块

函数或者其它语句都可以另存为.py
调用时候需要先放入路径，然后import name.然后调用 moto.moto(cycle)
``` python

# coding: utf-8
#name:moto

# In[ ]:

import time
import random
def moto(cycle):
    tik = time.time()
    count=0
    cycle=2**10
    x_inp=[]
    y_inp=[]
    x_out=[]
    y_out=[]
    #循环
    for i in range(cycle):
        #生成一个随机点
        x,y=random.random(),random.random()
        #判断是否在圆内
        if x**2+y**2<1:
            count+=1
            x_inp.append(x)
            y_inp.append(y)
        else:
            x_out.append(x)
            y_out.append(y)
    tok= time.time()
    pi = 4*count/cycle
    print(pi)
    print(tok-tik)


```

#### 首先查看路径
import sys
sys.path

路径的优先级是从上到下的，最上面的空是设置的工作路径


#### 将代码另存为.py

#### 将.py文件放入工作目录

#### import 模块

### import语句

### 包的管理

anaconda的直接使用conda命令即可。
管理员权限下打开cmd运行命令。
安装
- conda install packagename
更新
- conda update-all

### 导入自己编写的内容




### 赌徒必输练习

<!--Note-->
#### 赌徒必输理论
已知一赌徒，使用加倍加注法进行押注。假设该赌徒的胜率为50% 资本为N，尝试证明该赌徒最后必会输光。
加倍押注指的是，以一单位（假设此处为1元）作为第一场的押注，如果赢了，继续以一元押注，如果输了则以2元押注，2元押注如果输了则继续翻倍，直到赢。赢了后则再从一元开始押注。

``` python
import random
import matplotlib.pyplot as plt#画图的包，as后面是别名，方便调用
%matplotlib inline
def never_lose(dollar,cycle,d=0.5):
    # 设定一个资金曲线

    history = [dollar]
    # 初始化赌资倍数
    times = 0
    # 循环
    for i in range(cycle):
        # 确定压多少
        money=2**times
    #    if history[-1]>money:
    #        pool = money
    #    else:
    #        pool = history[-1]
        pool = money if history[-1]>money else history[-1]
        # 开盘，胜率050%，
        flag = random.random()
        # 计算赌资
        win = (1 if flag > d else -1)*pool
        history.append(history[-1]+win)
        # 重新调整下赌资倍数
        times = 0 if win>0 else (times+1)
        # 赌资为0，停止循环
        if history[-1]<=0:
            print("经过{}循环，输光了还剩下{}钱".format(i,history[-1]))
            break
    #循环结束，计算赌资
    print("经过{}循环，没输光，还剩下{}钱".format(len(history)-1,history[-1]))
    plt.plot(history)
```
<!--/Note-->

## 第九章 IO操作

IO表示input/output,也就是输入和输出

### 查看文件编码

为了文件的打开关闭更方便，也可以使用with语句来自动帮我们调用close()方法。
``` python
import chardet
#参数rb为使用二进制打开
with open("bikes.csv","rb") as f:#相当于try。。。finally f.close(),关闭文件
    data=f.read()
    print(chardet.detect(data))
#确认编码打开文件
f = open("bikes.csv",encoding= 'ISO-8859-1')
f = open("bikes.csv",encoding= 'ISO-8859-1')
f.readlines()
```
``` python
f.close()
```

### 操作文件和目录

``` python
import os
for x,y,z in os.walk(r"D:\python_workspace"):
    print(x)#返回文件夹内文件夹名称
    print(y)#返回目录内文件名称
    print(z)#返回文件夹内文件名称
```

## 第十章 日期和时间

## 第十一章 *类和面向对象


# python面向对象

### 1. 真实世界中的对象

函数可以把一些代码收集到能够反复使用的单元中，列表可以收集变量，对象则让这种收集的思想更向前迈进一步。对象可以把函数和数据收集在一起。

什么是对象？

对象是对现实事物的抽象，拿球举个例子，可以操作一个球，比如捡球、抛球、踢球或者充气。我们把这些操作称为动作。还可以通过指出球的颜色、大小和重量来描述一个球。这些就是球的属性。

真实世界的真实对象包括两个方面。
- 可以对它们做什么（动作）。
- 如果描述（属性或特征）。

### 2. python中的对象

在python中，一个对象的特征成为属性，动作称为方法。如果要建立一个球python版本或者模型，球就是一个对象，它有属性和方法。

- 球的属性可能包括球的颜色、球的大小、球的重量
- 球的方法包括kick、throw、inflate等操作

#### 什么是属性

属性就是你所知道的关于球的所有方面。球的属性就是一些信息

#### 什么是方法

方法就是可以对对象做的操作，它们是一些代码块，可以调用这些代码块来完成某个工作。其实，方法就是包含在对象中的函数。

函数能做到的，方法都可以做到，包括传递参数和返回值。

### 3. 创建对象

python中创建对象包括两步。

- 第一步是定义对象看上去什么样，会做点什么，也就是它的属性和方法。但是创建这个描述并不会真正创建一个对象。这有点像一个房子的蓝图。蓝图可以告诉你房子看上去怎么样，但是蓝图本身并不是一个房子。你不可能住在一个蓝图里。只能用它来建造真正的房子。实际上，可以使用蓝图盖很多的房子。在python中，对象的描述或蓝图称为一个类（class）。
- 第二步是使用类来建立一个真正的对象。这个对象称为这个类的一个实例（instance）

创建一个简单的Ball类


```python
class Ball:
    def bounce(self):
        if self.direction == "down":
            self.direction = "up"
```

创建一个对象实例

类定义并不是一个对象，这只是蓝图，现在来盖真正的房子。

上面创建的类中，球还没有任何属性，所以给它提供一些属性，这是为对象定义属性的一种方法


```python
class Ball:
    def bounce(self):
        if self.direction == "down":
            self.direction = "up"
myBall = Ball()
myBall.direction = "down"
myBall.color = "red"
myBall.size = "small"

print("I just created a ball.")
print("My ball is",myBall.size)
print("My ball is",myBall.color)
print("My ball's direction is",myBall.direction)

myBall.bounce()
print("Now the ball's direction is",myBall.direction)
```

    I just created a ball.
    My ball is small
    My ball is red
    My ball's direction is down
    Now the ball's direction is up
    

### 4. 初始化对象

创建球对象时，并没有在size、color或direction中填入任何内容。必须在创建对象之后填充这些内容。不过有一种方法可以在创建对象时设置属性。这称为初始化对象。

初始化表示“开始时做好准备”。在软件中对某个东西初始化时，就是把它设置成一种我们希望的状态或条件，以备使用。

创建类定义时，可以定义一个特定的方法，名为__init__()，只要创建这个类的一个新实例，就会运行这个方法。可以向__init__()方法传递参数，这样创建实例时就会把属性设置为你希望的值。


```python
class Ball:
    def __init__(self,color,size,direction):
        self.color = color
        self.size = size
        self.direction = direction
        
    def bounce(self):
        if self.direction == "down":
            self.direction = "up"
```


```python
myBall = Ball("red","small","down")

print("I just created a ball.")
print("My ball is",myBall.size)
print("My ball is",myBall.color)
print("My ball's direction is",myBall.direction)

myBall.bounce()
print("Now the ball's direction is",myBall.direction)
```

    I just created a ball.
    My ball is small
    My ball is red
    My ball's direction is down
    Now the ball's direction is up
    

### 5 . “魔法”方法：__str__()


```python
myBall
```




    <__main__.Ball at 0x16a0a0cdf60>



要改变这个显示，需要加入一个__str__()方法，让它返回你真正想打印的内容。这样一来，每次使用myBall时，它就会显示你想要的东西，这就是python中的一个“魔法”__xxxx__()类方法！

魔法方法是在你创建类时python自动包含的一些方法。我们会把它们叫做特殊方法。

我们已经知道，__init__()方法会在对象创建时完成初始化。每个对象都内置有一个__init__()方法。如果你在类定义中没有加入自己的__init__()方法，就会有这样一个内置方法接管，它的工作就是创建对象。

另一个特殊方法是__str__(),它会告诉python打印(print)一个对象时具体显示什么内容。


```python
class Ball:
    def __init__(self,color,size,direction):
        self.color = color
        self.size = size
        self.direction = direction
        
    def __str__(self):
        msg = "Hi,I'm a " + self.size + " "+ self.color + "ball!"
        return msg
myBall = Ball("red","small","down")
print(myBall)
```

    Hi,I'm a small redball!
    

### 6 .什么是self

你可能已经注意到，在类属性和方法定义中多处出现了"self"，self是什么意思？我们说过，可以使用蓝图盖很多个房子，使用一个类也可以创建多个对象实例，方法必须知道是哪个实例调用了它，self参数会告诉方法哪个对象调用它。这称为实例引用。

调用方法时，warrensBall.bounce()的括号里没有参数，但是方法里却又一个self参数。既然我们并没有传入任何东西，这个self参数从哪里来的？这是python处理对象的另外一个"魔法"。调用一个类方法时，究竟是哪个实例调用了这个方法？这个信息（也就是实例引用）会自动传递给方法。

self这个名字在python中没有任何特殊的含义。只不过所有人都使用这个实例引用名。这也是让代码更易读的一个约定。也可以把这个实例变量命名为你想要的任务名字，不过强烈建议你遵循这个约定，因为使用self能减少混乱。

### 7. 一个示例类--Hotdog

定义类，先定义__init__()方法，它会为热狗设置默认属性：


```python
class HotDog:
    def __init__(self):
        self.cooked_level = 0
        self.cooked_string = "Raw"
        self.condiments = []
```

先从一个没有加任何配料的生热狗开始，建立一个方法考热狗


```python
def cook(self,time):
    self.cooked_level = self.cooked_level + time
    if self.cooked_level > 8:
        self.cooked_string = "Charcoal"
    elif self.cooked_level > 5:
        self.cooked_string = "Well done"
    elif self.cooked_level > 3:
        self.cooked_string = "Medium"
    else:
        self.cooked_string = "Raw"
```

创建一个实例，并且检查它的属性


```python
class HotDog:
    def __init__(self):
        self.cooked_level = 0
        self.cooked_string = "Raw"
        self.condiments = []
    def cook(self,time):
        self.cooked_level = self.cooked_level + time
        if self.cooked_level > 8:
            self.cooked_string = "Charcoal"
        elif self.cooked_level > 5:
            self.cooked_string = "Well done"
        elif self.cooked_level > 3:
            self.cooked_string = "Medium"
        else:
            self.cooked_string = "Raw"
myDog = HotDog()
print(myDog.cooked_level)
print(myDog.cooked_string)
print(myDog.condiments)
```

    0
    Raw
    []
    

现在我们用cook方法


```python
class HotDog:
    def __init__(self):
        self.cooked_level = 0
        self.cooked_string = "Raw"
        self.condiments = []
    def cook(self,time):
        self.cooked_level = self.cooked_level + time
        if self.cooked_level > 8:
            self.cooked_string = "Charcoal"
        elif self.cooked_level > 5:
            self.cooked_string = "Well done"
        elif self.cooked_level > 3:
            self.cooked_string = "Medium"
        else:
            self.cooked_string = "Raw"
myDog = HotDog()
print(myDog.cooked_level)
print(myDog.cooked_string)
print(myDog.condiments)
print("Now I'm going to cook the hot dog")
myDog.cook(4)
print(myDog.cooked_level)
print(myDog.cooked_string)
```

    0
    Raw
    []
    Now I'm going to cook the hot dog
    4
    Medium
    

现在我们增加一些配料，另外还可以自己增加__str__()函数，让打印对象更为容易


```python
class HotDog:
    def __init__(self):
        self.cooked_level = 0
        self.cooked_string = "Raw"
        self.condiments = []
    def __str__(self):
        msg = "hot dog"
        if len(self.condiments)>0:
            msg = msg + " with "
        for i in self.condiments:
            msg = msg+i+", "
        msg = msg.strip(", ")
        msg = self.cooked_string+ " "+msg+"."
        return msg
    def cook(self,time):
        self.cooked_level = self.cooked_level + time
        if self.cooked_level > 8:
            self.cooked_string = "Charcoal"
        elif self.cooked_level > 5:
            self.cooked_string = "Well done"
        elif self.cooked_level > 3:
            self.cooked_string = "Medium"
        else:
            self.cooked_string = "Raw"
    def addCondiment(self,condiment):
        self.condiments.append(condiment)
        
myDog = HotDog()
print(myDog)
print("Cooking hot dog for 4 minutes...")
myDog.cook(4)
print(myDog)
print("Cooking hot dog for 3 more minutes...")
myDog.cook(3)
print(myDog)
print("What happens if I cook it for 10 more minutes?")
myDog.cook(10)
print(myDog)
print("Now,I'm going to add some stuff on my hot dog")
myDog.addCondiment("ketchup")
myDog.addCondiment("mustard")
print(myDog)
```

    Raw hot dog.
    Cooking hot dog for 4 minutes...
    Medium hot dog.
    Cooking hot dog for 3 more minutes...
    Well done hot dog.
    What happens if I cook it for 10 more minutes?
    Charcoal hot dog.
    Now,I'm going to add some stuff on my hot dog
    Charcoal hot dog with ketchup, mustard.
    

程序的第一部分创建了类。第二部分测试了烤这个虚拟热狗和添加配料的方法。


```python
class HotDog:
    def __init__(self):
        self.cooked_level = 0
        self.cooked_string = "Raw"
        self.condiments = []
    def __str__(self):
        msg = "hot dog"
        if len(self.condiments)>0:
            msg = msg + " with "
        for i in self.condiments:
            msg = msg+i+", "
        msg = msg.strip(", ")
        msg = self.cooked_string+ " "+msg+"."
        return msg
    def cook(self,time):
        self.cooked_level = self.cooked_level + time
        if self.cooked_level > 8:
            self.cooked_string = "Charcoal"
        elif self.cooked_level > 5:
            self.cooked_string = "Well done"
        elif self.cooked_level > 3:
            self.cooked_string = "Medium"
        else:
            self.cooked_string = "Raw"
    def addCondiment(self,condiment):
        self.condiments.append(condiment)
```

### 8. 多态和继承

#### 多态---同一个方法，不同的行为

多态是指对于不同的类，可以有同名的两个（或多个）方法。取决于这些方法分别应用到哪个类，它们可以有不同的行为。

假设你要建立一个程序做几何题，需要计算不同形状的面积，比如三角形和正方形


```python
class Triangle:
    def __init__(self,width,height):
        self.width = width
        self.height = height
    
    def getArea(self):
        area = self.width * self.height/2.0
        return area
    
class Square:
    def __init__(self,size):
        self.size = size 
        
    def getArea(self):
        area = self.size * self.size
        return area
```


```python
myTriangle = Triangle(4,5)
mySquare = Square(7)
```


```python
myTriangle.getArea()
```




    10.0




```python
mySquare.getArea()
```




    49



Triangle类和Square类都有一个名为getArea()的方法。所以，如果分别有这两个类的实例，这两个形状都使用了方法名getArea()，不过每个形状中这个方法做的工作不同。

#### 继承--向父母学习

在真实的世界中，人们可以从他们的父母或者其他亲戚那里继承一些东西。你可以继承一些特征，比如说红头发，或者可以继承像钱和财产之类的东西

在面向对象编程中，类可以从其他类继承属性和方法。这样就有了类的整个"家族"，这个"家族"中的每个类共享相同的属性和方法。这样一来，每次向"家族"增加新成员时就不必从头开始。

从其他类继承属性或方法的类称为派生类或子类。举个例子：假设我们要建立一个游戏，玩家一路上可以捡起不同的东西，比如食物、钱或衣服，可以建一个类，名为GameObject。GameObject类有name等属性和pickUp()等方法。所有游戏对象都有这些共同的方法和属性。

然后，可以为硬币建立一个子类。Coin类从GameObject派生。他要继承GameObject的属性和方法，所以Coin类会自动有一个name属性和pickUp()方法。Coin类还需要一个value属性和一个spend()方法。


```python
class GameObject:
    def __init__(self,name):
        self.name = name
        
    def pickup(self,player):
        if player =="xiaoming":
            print("little coin")
    

class Coin(GameObject):
    def __init__(self,value):
        GameObject.__init__(self,"coin")
        self.value = value
        
    def spend(self,buyer,seller):
        pass
```


```python
my_coin = Coin(45)
```


```python
my_coin.name
```




    'coin'




```python
my_coin.pickup("xiaoming")
```

    little coin
    


```python

```


## 第十二章 连接数据库


在 Python 里面进行数据分析或者清洗, 导出导入数据时, 有时候我们直接读取数据文件, 而有的时候我们则需要去连接数据库.  

本篇文章就针对一些常用的数据库 MySQL 和 SQLite3 的连接做一些演示.  
之所以加入 SQLite3 是因为 Python 有内置该数据库, 非常方便于使用.

### MySQL

在 Python 3 里面主要使用 MySQL 官方的 mysql-connector-python 和 pymysql 这两个库.  
在 Python 2 里, 还有一些常见的库, 但是有些没有继续支持3(好像最近MySQLdb也有3的版本了), 本篇主要讲 Python 3 因此以上面两个库为例.  

数据库的链接基本上都是大同小异, 但是很多细小的地方往往会导致一些不易查明的异常, 所以在这里做一个总结性的教程.  
这里不涉及数据库的SQL语句相关的内容.

##### 使用  mysql-connector-python 连接MySQL数据库.


```python
import mysql.connector
```

###### 创建数据库 "sampledb"


```python
def create_db_sampledb():
    config_root = {
        "host": "localhost",
        "user": "root",
        "password": "1234"}  # 创建root用户的链接配置
    sql =  "Create Database If Not Exists sampledb CHARSET=utf8 COLLATE=utf8_bin"
    try:
        conn =  mysql.connector.connect(**config_root)
        cursor = conn.cursor()
        cursor.execute(sql)
        conn.commit()
    finally:
        conn.close()
        
create_db_sampledb()
```

配置 sampledb 连接信息 (全局使用, 后面的操作均在该数据库里进行)


```python
mysql_config_sampledb ={
    "host":"127.0.0.1", 
    "database":"sampledb", 
    "user":"root", 
    "password":"1234"}
```

###### 创建表


```python
def create_table_sampletb():
    """如果该表不存在, 创建该表"""
    sql = (
        "Create Table If Not Exists sampletb( "
        "PassengerId int Primary key, "
        "Survived int(1), "
        "Pclass int(1), "
        "Name varchar(100), "
        "Sex varchar(10), "
        "Age int(3), "
        "SibSp int(1), "
        "Parch int(1), "
        "Ticket varchar(20), "
        "Fare float, "
        "Cabin varchar(100), "
        "Embarked varchar(10))")
    try:
        conn =  mysql.connector.connect(**mysql_config_sampledb)# 两个星号表示字典
        cursor = conn.cursor()
        cursor.execute(sql)
        conn.commit()
    finally:
        conn.close()
        
create_table_sampletb()
```

###### 删除表


```python
def drop_table_sampletb():
    """如果该表存在, 删除该表"""
    sql = "DROP TABLE IF EXISTS sampletb"
    try:
        conn =  mysql.connector.connect(**mysql_config_sampledb)
        cursor = conn.cursor()
        cursor.execute(sql)
        conn.commit()
    finally:
        conn.close()
        
drop_table_sampletb()
```


```python
create_table_sampletb()  # 重新建立该表
```

###### 插入数据


```python
import pandas as pd
```


```python
def insert_into_sampletb():
    df = pd.read_csv(r"C:\Users\CDAer\Desktop\施洪光\第六阶段python\python课件\python_basic\train.csv")
    df = df.where(~pd.isnull(df), other=None)#~表示反过来，pd.isnull(df)返回布尔值。前面有波浪线，所有有缺失值为~True=False
    
    sql = (
        "INSERT INTO sampletb "
        "(PassengerId,Survived,Pclass,Name,Sex,Age,SibSp,Parch,Ticket,Fare,Cabin,Embarked) "
        "VALUES (%s, %s, %s, %s, %s, %s, %s, %s, %s, %s, %s, %s)")
    try:
        conn = mysql.connector.connect(**mysql_config_sampledb)
        cursor = conn.cursor()
        # cursor.executemany(sql, multiple_data)  # 插入多条记录, 其中multiple_data为list, 其中每一条记录为一个元组. 
        # cursor.execut(sql, data)  # 插入单条数据, 其中data记录为一个元组. 
        for row in df.iterrows():
            li = row[1].values
            cursor.execute(sql, tuple(li))  # 此处为插入单条数据

        conn.commit()
    finally:
        conn.close()
        
insert_into_sampletb()
```

更新数据同理

###### 查询数据


```python
select_sampletb = "SELECT * FROM sampletb LIMIT 100"  # 查询数据
select_sampletb_columns = "SHOW columns FROM sampletb"  # 查看表列名
```


```python
def select_from_sampletb(config, sql):
    """查询语句, 输入数据库的链接信息(字典)以及查询语句.
    打印查询条数, 并返回查询的结果.
    """
    try:
        conn = mysql.connector.connect(**config)
        cursor = conn.cursor()
        cursor.execute(sql)
        result = cursor.fetchall()
    finally:
        conn.close()
    return result
```


```python
result = select_from_sampletb(mysql_config_sampledb, select_sampletb)
type(result)
```




    list




```python
print(result[0:3])
```

    [(1, 0, 3, bytearray(b'Braund, Mr. Owen Harris'), bytearray(b'male'), 22, 1, 0, bytearray(b'A/5 21171'), 7.25, None, bytearray(b'S')), (2, 1, 1, bytearray(b'Cumings, Mrs. John Bradley (Florence Briggs Thayer)'), bytearray(b'female'), 38, 1, 0, bytearray(b'PC 17599'), 71.2833, bytearray(b'C85'), bytearray(b'C')), (3, 1, 3, bytearray(b'Heikkinen, Miss. Laina'), bytearray(b'female'), 26, 0, 0, bytearray(b'STON/O2. 3101282'), 7.925, None, bytearray(b'S'))]
    


```python
select_from_sampletb(mysql_config_sampledb, select_sampletb_columns)
```




    [('PassengerId', 'int(11)', 'NO', 'PRI', None, ''),
     ('Survived', 'int(1)', 'YES', '', None, ''),
     ('Pclass', 'int(1)', 'YES', '', None, ''),
     ('Name', 'varchar(100)', 'YES', '', None, ''),
     ('Sex', 'varchar(10)', 'YES', '', None, ''),
     ('Age', 'int(3)', 'YES', '', None, ''),
     ('SibSp', 'int(1)', 'YES', '', None, ''),
     ('Parch', 'int(1)', 'YES', '', None, ''),
     ('Ticket', 'varchar(20)', 'YES', '', None, ''),
     ('Fare', 'float', 'YES', '', None, ''),
     ('Cabin', 'varchar(100)', 'YES', '', None, ''),
     ('Embarked', 'varchar(10)', 'YES', '', None, '')]



##### 使用 pymysql 连接MySQL数据库.  
与使用 mysql-connector-python 非常相似


```python
import pymysql 
```

###### 创建数据库 "sampledb2"


```python
def creat_database_sampledb2():
    config_root = {
        "host": "localhost",
        "user": "root",
        "password": "1234"}
    sql = "Create Database If Not Exists sampledb2 CHARSET=utf8 COLLATE=utf8_bin"
    conn = pymysql.connect(**config_root)  # 打开数据库连接
    try:
        with conn.cursor() as cursor:  # 使用cursor()方法获取操作游标,并在语句结束自动关闭
            cursor.execute(sql)  # 执行SQL
            conn.commit()  # 提交
    finally:
        conn.close()

creat_database_sampledb2()
```

配置 sampledb2 连接信息 (全局使用, pymysql后面的操作均在该数据库里进行)


```python
pymysql_config_sampledb2 ={
    "host":"127.0.0.1", 
    "database":"sampledb2", 
    "user":"root", 
    "password":"1234"}
```

###### 创建表


```python
def create_table_sampletb2():
    """如果该表不存在, 创建该表"""
    sql = (
        "Create Table If Not Exists sampletb2( "
        "PassengerId int Primary key, "
        "Survived int(1), "
        "Pclass int(1), "
        "Name varchar(100), "
        "Sex varchar(10), "
        "Age int(3), "
        "SibSp int(1), "
        "Parch int(1), "
        "Ticket varchar(20), "
        "Fare float, "
        "Cabin varchar(100), "
        "Embarked varchar(10))")
    conn = pymysql.connect(**pymysql_config_sampledb2)  # 打开数据库连接, 官方并没有把这个写在try语句并有解释.
    try:
        with conn.cursor() as cursor:
            cursor.execute(sql)
            conn.commit()
    finally:
        conn.close()

create_table_sampletb2()
```

###### 删除表


```python
def drop_table_sampletb2():
    """如果该表存在, 删除该表"""
    sql = "DROP TABLE IF EXISTS sampletb2"
    conn = pymysql.connect(**pymysql_config_sampledb2)
    try:
        with conn.cursor() as cursor:
            cursor.execute(sql)
            conn.commit()
    finally:
        conn.close()

drop_table_sampletb2()
```


```python
create_table_sampletb2()  # 重新建立该表
```

###### 插入数据


```python
import pandas as pd
```


```python
def insert_into_sampletb2():
    df = pd.read_csv("/WorkSpace/Data/titanic/train.csv")
    df = df.where(~pd.isnull(df), other=None)
    
    sql = (
        "INSERT INTO sampletb2 "
        "(PassengerId,Survived,Pclass,Name,Sex,Age,SibSp,Parch,Ticket,Fare,Cabin,Embarked) "
        "VALUES (%s, %s, %s, %s, %s, %s, %s, %s, %s, %s, %s, %s)")
    conn = pymysql.connect(**pymysql_config_sampledb2)
    try:
        with conn.cursor() as cursor:
            # cursor.executemany(sql, multiple_data)
            # cursor.execut(sql, data)
            for row in df.iterrows():
                li = row[1].values
                cursor.execute(sql, tuple(li))  # 此处为插入单条数据
            conn.commit()
    finally:
        conn.close()

insert_into_sampletb2()
```

更新数据同理

###### 查询数据


```python
select_sampletb2 = "SELECT * FROM sampletb2 LIMIT 100"  # 查询数据
select_sampletb2_columns = "SHOW columns FROM sampletb2"  # 查看表列名
```


```python
def select_from_sampletb2(config, sql):

    conn = pymysql.connect(**config)
    try:
        with conn.cursor() as cursor:
            cursor.execute(sql)
            result = cursor.fetchall()
    finally:
        conn.close()
    return result
```


```python
result = select_from_sampletb2(pymysql_config_sampledb2, select_sampletb2)
type(result)
```




    tuple




```python
print(result[0:3])
```

    ((1, 0, 3, 'Braund, Mr. Owen Harris', 'male', 22, 1, 0, 'A/5 21171', 7.25, None, 'S'), (2, 1, 1, 'Cumings, Mrs. John Bradley (Florence Briggs Thayer)', 'female', 38, 1, 0, 'PC 17599', 71.2833, 'C85', 'C'), (3, 1, 3, 'Heikkinen, Miss. Laina', 'female', 26, 0, 0, 'STON/O2. 3101282', 7.925, None, 'S'))
    


```python
select_from_sampletb2(pymysql_config_sampledb2, select_sampletb2_columns)
```




    (('PassengerId', 'int(11)', 'NO', 'PRI', None, ''),
     ('Survived', 'int(1)', 'YES', '', None, ''),
     ('Pclass', 'int(1)', 'YES', '', None, ''),
     ('Name', 'varchar(100)', 'YES', '', None, ''),
     ('Sex', 'varchar(10)', 'YES', '', None, ''),
     ('Age', 'int(3)', 'YES', '', None, ''),
     ('SibSp', 'int(1)', 'YES', '', None, ''),
     ('Parch', 'int(1)', 'YES', '', None, ''),
     ('Ticket', 'varchar(20)', 'YES', '', None, ''),
     ('Fare', 'float', 'YES', '', None, ''),
     ('Cabin', 'varchar(100)', 'YES', '', None, ''),
     ('Embarked', 'varchar(10)', 'YES', '', None, ''))



***
### SQLite3


```python
import sqlite3
```

在使用SQLite3去连接一个数据库时, 如果该数据库存在, 那么就会连接上这个数据库.  
如果这个数据库不存在, 那么会创建这个数据库, 并连接上.

设置一个路径, 作为数据库的路径


```python
sqlite3_path = "sqlite_sample.db"
```

###### 创建一个数据库, 并且创建一个表.


```python
def create_sqlite_sampletb(db_path):
    sql = (
        "Create Table If Not Exists sampletb( "
        "PassengerId int Primary key, "
        "Survived int(1), "
        "Pclass int(1), "
        "Name varchar(100), "
        "Sex varchar(10), "
        "Age int(3), "
        "SibSp int(1), "
        "Parch int(1), "
        "Ticket varchar(20), "
        "Fare float, "
        "Cabin varchar(100), "
        "Embarked varchar(10))")
    
    with sqlite3.connect(db_path) as conn:
        cursor = conn.cursor()
        cursor.execute(sql)
        conn.commit()

create_sqlite_sampletb(sqlite3_path)
```

若想删除数据库, 直接删除.db文件就行了

###### 删除表


```python
def drop_sqlite_sampletb(db_path):
    sql = "DROP TABLE IF EXISTS sampletb"
    
    with sqlite3.connect(db_path) as conn:
        cursor = conn.cursor()
        cursor.execute(sql)
        conn.commit()

drop_sqlite_sampletb(sqlite3_path)
```


```python
create_sqlite_sampletb(sqlite3_path)  # 新建表
```

查看当前数据库中的所有的表


```python
def select_all_tables(db_path):
    sql = "SELECT name FROM sqlite_master WHERE type='table' ORDER BY name"  # 或者select * 查看表结构
    with sqlite3.connect(db_path) as conn:
        cursor = conn.cursor()
        cursor.execute(sql)
        conn.commit()
    return cursor.fetchall()

select_all_tables(sqlite3_path)
```




    [('sampletb',)]



###### 插入数据


```python
def insert_into_sqlite_sampletb(db_path):
    df = pd.read_csv("/WorkSpace/Data/titanic/train.csv")
    df = df.where(~pd.isnull(df), other=None)
    
    sql = (
        "INSERT INTO sampletb "
        "(PassengerId,Survived,Pclass,Name,Sex,Age,SibSp,Parch,Ticket,Fare,Cabin,Embarked) "
        "VALUES (?, ?, ?, ?, ?, ?, ?, ?, ?, ?, ?, ?)")
    with sqlite3.connect(db_path) as conn:
        cursor = conn.cursor()
        # cursor.executemany(sql, multiple_data)
        # cursor.execut(sql, data)
        for row in df.iterrows():
            li = row[1].values
            cursor.execute(sql, tuple(li))
        conn.commit()

insert_into_sqlite_sampletb(sqlite3_path)
```

###### 查询数据


```python
def select_sqllite_sampletb(db_path):
    sql = "SELECT * FROM sampletb LIMIT 100"

    with sqlite3.connect(db_path) as conn:
        cursor = conn.cursor()
        cursor.execute(sql)
        conn.commit()
    return cursor.fetchall()
```


```python
result = select_sqllite_sampletb(sqlite3_path)
type(result)
```




    list




```python
print(result[0:3])
```

    [(1, 0, 3, 'Braund, Mr. Owen Harris', 'male', 22, 1, 0, 'A/5 21171', 7.25, None, 'S'), (2, 1, 1, 'Cumings, Mrs. John Bradley (Florence Briggs Thayer)', 'female', 38, 1, 0, 'PC 17599', 71.2833, 'C85', 'C'), (3, 1, 3, 'Heikkinen, Miss. Laina', 'female', 26, 0, 0, 'STON/O2. 3101282', 7.925, None, 'S')]
    

***
### 利用Pandas和数据库交互

在较多情景下, 可以直接去数据库读取我们想要的数据, 并转化为 Pandas 中的 DataFrame 数据格式.


```python
import pandas as pd
import sqlalchemy
```

###### MySQL + mysql-connector-python


```python
import mysql.connector
```


```python
mysql_engine = sqlalchemy.create_engine('mysql+mysqlconnector://root:1234@localhost/sampledb', encoding='utf-8')
pd.read_sql('show tables', mysql_engine)
```




<div>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>Tables_in_sampledb</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>sampletb</td>
    </tr>
  </tbody>
</table>
</div>



###### MySQL + pymysql


```python
import pymysql
```


```python
pymysql_engine = sqlalchemy.create_engine('mysql+pymysql://root:1234@localhost/sampledb', encoding='utf-8')
pd.read_sql("SELECT * FROM sampletb LIMIT 10", pymysql_engine)
```




<div>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>PassengerId</th>
      <th>Survived</th>
      <th>Pclass</th>
      <th>Name</th>
      <th>Sex</th>
      <th>Age</th>
      <th>SibSp</th>
      <th>Parch</th>
      <th>Ticket</th>
      <th>Fare</th>
      <th>Cabin</th>
      <th>Embarked</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>1</td>
      <td>0</td>
      <td>3</td>
      <td>Braund, Mr. Owen Harris</td>
      <td>male</td>
      <td>22.0</td>
      <td>1</td>
      <td>0</td>
      <td>A/5 21171</td>
      <td>7.2500</td>
      <td>None</td>
      <td>S</td>
    </tr>
    <tr>
      <th>1</th>
      <td>2</td>
      <td>1</td>
      <td>1</td>
      <td>Cumings, Mrs. John Bradley (Florence Briggs Th...</td>
      <td>female</td>
      <td>38.0</td>
      <td>1</td>
      <td>0</td>
      <td>PC 17599</td>
      <td>71.2833</td>
      <td>C85</td>
      <td>C</td>
    </tr>
    <tr>
      <th>2</th>
      <td>3</td>
      <td>1</td>
      <td>3</td>
      <td>Heikkinen, Miss. Laina</td>
      <td>female</td>
      <td>26.0</td>
      <td>0</td>
      <td>0</td>
      <td>STON/O2. 3101282</td>
      <td>7.9250</td>
      <td>None</td>
      <td>S</td>
    </tr>
    <tr>
      <th>3</th>
      <td>4</td>
      <td>1</td>
      <td>1</td>
      <td>Futrelle, Mrs. Jacques Heath (Lily May Peel)</td>
      <td>female</td>
      <td>35.0</td>
      <td>1</td>
      <td>0</td>
      <td>113803</td>
      <td>53.1000</td>
      <td>C123</td>
      <td>S</td>
    </tr>
    <tr>
      <th>4</th>
      <td>5</td>
      <td>0</td>
      <td>3</td>
      <td>Allen, Mr. William Henry</td>
      <td>male</td>
      <td>35.0</td>
      <td>0</td>
      <td>0</td>
      <td>373450</td>
      <td>8.0500</td>
      <td>None</td>
      <td>S</td>
    </tr>
    <tr>
      <th>5</th>
      <td>6</td>
      <td>0</td>
      <td>3</td>
      <td>Moran, Mr. James</td>
      <td>male</td>
      <td>NaN</td>
      <td>0</td>
      <td>0</td>
      <td>330877</td>
      <td>8.4583</td>
      <td>None</td>
      <td>Q</td>
    </tr>
    <tr>
      <th>6</th>
      <td>7</td>
      <td>0</td>
      <td>1</td>
      <td>McCarthy, Mr. Timothy J</td>
      <td>male</td>
      <td>54.0</td>
      <td>0</td>
      <td>0</td>
      <td>17463</td>
      <td>51.8625</td>
      <td>E46</td>
      <td>S</td>
    </tr>
    <tr>
      <th>7</th>
      <td>8</td>
      <td>0</td>
      <td>3</td>
      <td>Palsson, Master. Gosta Leonard</td>
      <td>male</td>
      <td>2.0</td>
      <td>3</td>
      <td>1</td>
      <td>349909</td>
      <td>21.0750</td>
      <td>None</td>
      <td>S</td>
    </tr>
    <tr>
      <th>8</th>
      <td>9</td>
      <td>1</td>
      <td>3</td>
      <td>Johnson, Mrs. Oscar W (Elisabeth Vilhelmina Berg)</td>
      <td>female</td>
      <td>27.0</td>
      <td>0</td>
      <td>2</td>
      <td>347742</td>
      <td>11.1333</td>
      <td>None</td>
      <td>S</td>
    </tr>
    <tr>
      <th>9</th>
      <td>10</td>
      <td>1</td>
      <td>2</td>
      <td>Nasser, Mrs. Nicholas (Adele Achem)</td>
      <td>female</td>
      <td>14.0</td>
      <td>1</td>
      <td>0</td>
      <td>237736</td>
      <td>30.0708</td>
      <td>None</td>
      <td>C</td>
    </tr>
  </tbody>
</table>
</div>



###### SQLite3


```python
sqlite_engine = sqlalchemy.create_engine('sqlite:////WorkSpace/Data/sqlite_sample.db', encoding='utf-8')
pd.read_sql("SELECT * FROM sampletb LIMIT 10", sqlite_engine)
```




<div>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>PassengerId</th>
      <th>Survived</th>
      <th>Pclass</th>
      <th>Name</th>
      <th>Sex</th>
      <th>Age</th>
      <th>SibSp</th>
      <th>Parch</th>
      <th>Ticket</th>
      <th>Fare</th>
      <th>Cabin</th>
      <th>Embarked</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>1</td>
      <td>0</td>
      <td>3</td>
      <td>Braund, Mr. Owen Harris</td>
      <td>male</td>
      <td>22.0</td>
      <td>1</td>
      <td>0</td>
      <td>A/5 21171</td>
      <td>7.2500</td>
      <td>None</td>
      <td>S</td>
    </tr>
    <tr>
      <th>1</th>
      <td>2</td>
      <td>1</td>
      <td>1</td>
      <td>Cumings, Mrs. John Bradley (Florence Briggs Th...</td>
      <td>female</td>
      <td>38.0</td>
      <td>1</td>
      <td>0</td>
      <td>PC 17599</td>
      <td>71.2833</td>
      <td>C85</td>
      <td>C</td>
    </tr>
    <tr>
      <th>2</th>
      <td>3</td>
      <td>1</td>
      <td>3</td>
      <td>Heikkinen, Miss. Laina</td>
      <td>female</td>
      <td>26.0</td>
      <td>0</td>
      <td>0</td>
      <td>STON/O2. 3101282</td>
      <td>7.9250</td>
      <td>None</td>
      <td>S</td>
    </tr>
    <tr>
      <th>3</th>
      <td>4</td>
      <td>1</td>
      <td>1</td>
      <td>Futrelle, Mrs. Jacques Heath (Lily May Peel)</td>
      <td>female</td>
      <td>35.0</td>
      <td>1</td>
      <td>0</td>
      <td>113803</td>
      <td>53.1000</td>
      <td>C123</td>
      <td>S</td>
    </tr>
    <tr>
      <th>4</th>
      <td>5</td>
      <td>0</td>
      <td>3</td>
      <td>Allen, Mr. William Henry</td>
      <td>male</td>
      <td>35.0</td>
      <td>0</td>
      <td>0</td>
      <td>373450</td>
      <td>8.0500</td>
      <td>None</td>
      <td>S</td>
    </tr>
    <tr>
      <th>5</th>
      <td>6</td>
      <td>0</td>
      <td>3</td>
      <td>Moran, Mr. James</td>
      <td>male</td>
      <td>NaN</td>
      <td>0</td>
      <td>0</td>
      <td>330877</td>
      <td>8.4583</td>
      <td>None</td>
      <td>Q</td>
    </tr>
    <tr>
      <th>6</th>
      <td>7</td>
      <td>0</td>
      <td>1</td>
      <td>McCarthy, Mr. Timothy J</td>
      <td>male</td>
      <td>54.0</td>
      <td>0</td>
      <td>0</td>
      <td>17463</td>
      <td>51.8625</td>
      <td>E46</td>
      <td>S</td>
    </tr>
    <tr>
      <th>7</th>
      <td>8</td>
      <td>0</td>
      <td>3</td>
      <td>Palsson, Master. Gosta Leonard</td>
      <td>male</td>
      <td>2.0</td>
      <td>3</td>
      <td>1</td>
      <td>349909</td>
      <td>21.0750</td>
      <td>None</td>
      <td>S</td>
    </tr>
    <tr>
      <th>8</th>
      <td>9</td>
      <td>1</td>
      <td>3</td>
      <td>Johnson, Mrs. Oscar W (Elisabeth Vilhelmina Berg)</td>
      <td>female</td>
      <td>27.0</td>
      <td>0</td>
      <td>2</td>
      <td>347742</td>
      <td>11.1333</td>
      <td>None</td>
      <td>S</td>
    </tr>
    <tr>
      <th>9</th>
      <td>10</td>
      <td>1</td>
      <td>2</td>
      <td>Nasser, Mrs. Nicholas (Adele Achem)</td>
      <td>female</td>
      <td>14.0</td>
      <td>1</td>
      <td>0</td>
      <td>237736</td>
      <td>30.0708</td>
      <td>None</td>
      <td>C</td>
    </tr>
  </tbody>
</table>
</div>



