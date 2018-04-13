# Python numpy

## 1.1Python科学计算的介绍

参考资料： http://old.sebug.net/paper/books/scipydoc/numpy_intro.html

http://www.numpy.org/

numpy是一个与数学模型构建、定量分析方法以及利用计算机分析和解决科学问题相关领域。

常用库： Numpy Scipy Pandas matplotlib

## 1.2 Numpy之ndarray对象

标准安装的Python中用列表(list)保存一组值，可以用来当作数组使用，不过由于列表的元素可以是任何对象，因此列表中所保存的是对象的指针。这样为了保存一个简单的[1,2,3]，需要有3个指针和三个整数对象。对于数值运算来说这种结构显然比较浪费内存和CPU计算时间。

此外Python还提供了一个array模块，array对象和列表不同，它直接保存数值，和C语言的一维数组比较类似。但是由于它不支持多维，也没有各种运算函数，因此也不适合做数值运算。

NumPy的诞生弥补了这些不足，NumPy提供了两种基本的对象：ndarray（N-dimensional array object）和 ufunc（universal function object）。ndarray(下文统一称之为数组)是存储单一数据类型的多维数组，而ufunc则是能够对数组进行处理的函数。

## 1.3 ndarray计算速度

## 1.4 ndarray基本操作

### 1.4.1 导入模块

导入Numpy模块

```python
import numpy as np
```


#### import Numpy as np

### 1.4.2 对data进行数学操作

#### 1. 生成随机数
np.random.randn(2,3)

```python
# 产生随机数，参数控制几行几列
data = np.random.randn(2,3)
data
```
与np.arange()相比，可以模拟出更加符合要求的随机数。

#### 2. 对data进行数学操作
因为是数组，会自动广播到所有的元素中。

### 1.4.3 ndarray的属性方法

#### 1.创建以及结构变换
np.array([1,2],[3,,4])

``` python
#生成11等分的0-1的12个数
np.linspace(0,1,12)
#生成等差序列
a=np.arange(12)
#生成等比数列 10^0-10^2有20个元素的等比数列
 np.logspace(0, 2, 20)
```
NumPy 提供了常用的对 ndarray 进行变换的方法.

- np.reshape: 返回一个按照给定的维度改变的 ndarray.

- np.resize: 在原位修改 ndarray 的维度.

- np.repeat: 复制 ndarray 的每个元素的值, 返回一个延长的 ndarray, 需要传入复制的次数作为参数. 当 ndarray 不是一维的时候, 返回的 ndarray 也会是一维的.
``` python
# 新生成一个对象，但是不修改原对象
a.reshape((2,6))
```

np.ones, np.ones_like
np.zeros, np.zeros_like
创建一个数组, 其中的元素全为 1. np.ones 根据参数设定的纬度创建一个元素为 1 的数组, 而 np.ones_like 则根据一个已有的数组创建和其有相同纬度的元素全为 1 的数组.

``` python
np.ones((4, 3))
np.ones_like(data)
```

#### 2. 与列表区别
ndarray内元素只能是同类型的。

#### 3. 查看元素个数
data.size

#### 4. 查看结构（几行几列）
data.shape
查看维数
data.ndim

#### 5. 查看元素类型
data.dtype

### 1.4.4 基础切片索引

所有切片索引都可以用来修改元素

#### 1. 切片方式与Python标准方法相同
a[5]、a[:5]、a[-1]、a[1:-1:]#间隔为2

``` python
>>> a = np.arange(10)
>>> a[5]    # 用整数作为下标可以获取数组中的某个元素
5
>>> a[3:5]  # 用范围作为下标获取数组的一个切片，包括a[3]不包括a[5]
array([3, 4])
>>> a[:5]   # 省略开始下标，表示从a[0]开始
array([0, 1, 2, 3, 4])
>>> a[:-1]  # 下标可以使用负数，表示从数组后往前数
array([0, 1, 2, 3, 4, 5, 6, 7, 8])
>>> a[2:4] = 100,101    # 下标还可以用来修改元素的值
>>> a
array([  0,   1, 100, 101,   4,   5,   6,   7,   8,   9])
>>> a[1:-1:2]   # 范围中的第三个参数表示步长，2表示隔一个元素取一个元素
array([  1, 101,   5,   7])
>>> a[::-1] # 省略范围的开始下标和结束下标，步长为-1，整个数组头尾颠倒
array([  9,   8,   7,   6,   5,   4, 101, 100,   1,   0])
>>> a[5:1:-2] # 步长为负数时，开始下标必须大于结束下标
array([  5, 101])
```

#### 2. 与python列表序列不同，通过下标获取的新数组是原始数组的一个视图，与原始数组共享一块数据空间。

``` python
>>>b = a[3:7] # 通过下标范围产生一个新的数组b，b和a共享同一块数据空间
>>> b
array([101,   4,   5,   6])
>>> b[2] = -10 # 将b的第2个元素修改为-10
>>> b
array([101,   4, -10,   6])
>>> a # a的第5个元素也被修改为10
array([  0,   1, 100, 101,   4, -10,   6,   7,   8,   9])
```


#### 3. 使用整数数列
x[[3,3,1]]

``` python 
>>>x = np.arange(10,1,-1)
>>> x
array([10,  9,  8,  7,  6,  5,  4,  3,  2])
>>> x[[3, 3, 1, 8]] # 获取x中的下标为3, 3, 1, 8的4个元素，组成一个新的数组
array([7, 7, 9, 2])
>>> b = x[np.array([3,3,-3,8])]  #下标可以是负数
>>> b[2] = 100
>>> b
array([7, 7, 100, 2])
>>> x   # 由于b和x不共享数据空间，因此x中的值并没有改变
array([10,  9,  8,  7,  6,  5,  4,  3,  2])
>>> x[[3,5,1]] = -1, -2, -3 # 整数序列下标也可以用来修改元素的值
>>> x
array([10, -3,  8, -1,  6, -2,  4,  3,  2])
```


#### 4. 使用布尔数组
x[[True,False,True]]
从头开始匹配，不够的部分默认为false

``` python

>>>x = np.arange(5,0,-1)
>>> x
array([5, 4, 3, 2, 1])
>>> x[np.array([True, False, True, False, False])]
>>> # 布尔数组中下标为0，2的元素为True，因此获取x中下标为0,2的元素
array([5, 3])
>>> x[[True, False, True, False, False]]
>>> # 如果是布尔列表，则把True当作1, False当作0，按照整数序列方式获取x中的元素
array([4, 5, 4, 5, 5])
>>> x[np.array([True, False, True, True])]
>>> # 布尔数组的长度不够时，不够的部分都当作False
array([5, 3, 2])
>>> x[np.array([True, False, True, True])] = -1, -2, -3
>>> # 布尔数组下标也可以用来修改元素
>>> x
array([-1,  4, -2, -3,  1])

```

#### 5. 通过布尔运算切片
x[x>0.5]

### 1.4.5 多维数组切片索引
两个轴方向，分别进行切片，中间用逗号隔开。
a[2::2,2::2]

``` python
#多维数组的创建方式和显示方式
>>>arr2d = np.array([[1,2,3],[4,5,6],[7,8,9]])
>>>arr2d

array([[1, 2, 3],
       [4, 5, 6],
       [7, 8, 9]])
```

### 1.4.6 布尔型索引

#### 1. ~表示T和F反过来
~("a"=="a")结果是False

#### 2. ！= 不等于

## 1.5 数组运算

### 1. 与数字的运算
广播到每一个元素

### 2. 数组函数
np.sqrt(ndarray)#开方
np.exp(ndarray)#e为底的元素次幂
np.maximum(ndarr_x,ndarr_y)#对应元素比较，留下大的
np.where(ndarray > 0,2,-2)#if 布尔运算 then 2 else -1

### 3. 数组方法
ndarray.mean(axis=1)#按照行求均值
ndarray.sum(axis=0)#按照列求和
ndarray.cumsum(axis=0)#按照列累加
ndarray.cumprod(axis=1)#按照行累乘

### 4. 排序
ndarray.sort(axis=1)

## 1.6 日期和时间的包

### 1. from datetime import datetime

用来计算时间
``` python
start = datetime.now()
c = function(x)
delta = datetime.now() - start
```

### 2. import time

``` python
time.clock()
```
