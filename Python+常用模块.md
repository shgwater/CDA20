# Python 常用模块

## 1. random模块

### 1.1 导入模块
import random

### 1.2 random.random()
生成一个从0到1的随机浮点数

### 1.3 random.uniform(10,20)
生成指点范围内，也就是10到20（包括10和20，且位置可以互换）之间的随机数

### 1.4 random.randint(a,b)
生成a到b之间的整数

### 1.5 random.randrange([start],stop[,step])
从指定集合中抽取随机数，

### 1.6 random.choice(sequence)
从序列中获取一个随机元素，序列可以使list、字符串等.
与np.random.choice(a,size=None..)相比，只能抽一个

### 1.7 random.shuffle(x[,random])
x为列表，用于将列表打乱

### 1.8 random.sample(seqnence,k)
从制定序列中获取指定长度的片段。

### 1.9 random.randint()
随机整数

## 2. time模块

### 2.1 导入模块
import time

### 2.2 time.time()
返回当前时间戳

### 2.3 time.localtime()
格式化时间戳为本地时间

### 2.4 time.asctime(time.localtime)
接受时间元组并返回一个可读的字符串

### 2.5 time.ctime()
时间戳转化为asctime的格式，可读

### 2.6 time.strftime("%a %b %d %H:%M:%S %Y", time.localtime())
格式化时间元组

### 2.7 time.sleep()
进程挂起时间。

## 3. datetime模块

### 3.1 导入模块
import datetime

### 3.2 datetime.datetime.now()
 获取当前datetime

### 3.3 datetime.date.today()
获取当天date，返回2018,4,8

### 3.4 获取明天/前n天
datetime.date.today()+datatime.timedelta(days=1)

### 3.5 两个datetime的时间差
相减返回时间戳

### 3.6 关系转换

#### 3.6.1 datetime->string
datetime.datetime.now().strftime("%Y-%m-%d %H:%M:%S")

#### 3.6.2 string->datetime
datetime.datetime.strptime("2014-12-31 18:20:10", "%Y-%m-%d %H:%M:%S")

#### 3.6.3 datetime->timestamp
now = datetime.datetime.now()
timestamp = time.mktime(now.timetuple())
timestamp

#### 3.6.3 timestamp->datetime
datetime.datetime.fromtimestamp(1421077403.0)

#### 3.6.4 datetime->date
datetime.datetime.now().date()

#### 3.6.5 date->datetime
today = datetime.date.today()
datetime.datetime.combine(today, datetime.time())
