# numpy类型dtype
    bool_
    
    (u)int8
    (u)int16
    (u)int32
    (u)int64

    float16
    float32
    float64

    complex64   双32位浮点数
    complex128  双64位浮点数

# numpy数组属性
|属性|说明|
|:----:|:----:|
|ndim|维度|
|shape|形状|
|dtype|数据类型|
|real|实部|
|imag|虚部|
# numpy创建

```numpy.identity(shape,dtype=Nonne)``` 单位矩阵

|函数|说明|
|:----:|:----:|
|empty|未初始化的数组|
|zeros|元素全为0|
|ones|元素全为1|

其中参数说明

|参数|说明|
|:----:|:----:|
|shape|形状|
|dtype|数据类型，可选|
|order|存储中"C"行优先，"F"优先，可选|


### numpy.arange(start, stop, step, dtype)
值域为``[start,stop)``的数组，步长为``step``，数据类型为``dtype``
### np.linspace(start, stop, num=50, endpoint=True, retstep=False, dtype=None)
创建等差数列
值域从``start``到``stop``
元素数量为``num``
``endpoint``表示元素中是否包含stop
``retstep``是否包含步长  ``a[0]``为``array`` a[1]为``step``

### np.logspace(start, stop, num=50, endpoint=True, base=10.0, dtype=None)
|参数|说明|
|:----:|:----:|
|start|起始值为base**start|
|stop|终止值为base**stop|
|num|元素个数|
|endpoint|是否包含stop|
|base|base|
|dtype|类型|


# numpy切片
左闭右开
```python
import numpy as np
a = np.arange(10)
print(a)  # [0 1 2 3 4 5 6 7 8 9]
print(a[2:6:2])  # [2 4]
print(a[slice(2, 6, 2)])  # [2 4]
print(a[:8:2])  # [0 2 4 6]
print(a[::2])  # [0 2 4 6 8]
```
``...``省略号省略某一维度

# numpy迭代器numpy.nditer
buxiangxie
# numpy数组操作
### 修改数组形状
- numpy.reshape(arr, newshape, order='C')
- arr.reshape(newshape,order='C')
    - order：'C' -- 按行，'F' -- 按列，'A' -- 原顺序，'k' -- 元素在内存中的出现顺序。
### 翻转数组
### 修改数组维度
### 连接数组
### 分割数组
### 数组元素的添加与删除


# numpy位运算
bitwise_and
bitwise_or
bitwise_xor
invert
left_shift
right_shift
binary_repr(a,bit_nums)

# numpy常用函数
- sin arcsin cos arccos tan arctan ...

- ```numpy.around(arr,decimals = 0)```
    - decimals:四舍五入到小数点右侧位数

- ```numpy.floor()``` 向下取整
- ```numpy.ceil()``` 向上取整
- ```numpy.amin()```
- ```numpy.amax()```
- ```numpy.argmin()```
- ```numpy.argmin()```
- ```numpy.ptp()```  ```amax()-amin()```
- ```numpy.percentile(arr,q,axis)``` 求p百分位数
    - arr:数组
    - q:百分比
    - axis：坐标轴
- ```numpy.median()``` 中位数
- ```numpy.mean()``` 算数平均值
- ```numpy.average(arr,axis,weights,returned=False)``` 加权平均值
    - returned=True 则返回权重sum(weights)
- ```numpy.std()``` 标准差
    - np.sqrt(np.mean((a-np.mean(a))**2))
- ```numpy.var()``` 方差

- ```numpy.sort(arr,axis,kind='quicksort',order)```
    - a: 要排序的数组
    - axis: 沿着它排序数组的轴，如果没有数组会被展开，沿着最后的轴排序， axis=0 按列排序- - axis
    - kind: 默认为'quicksort'（快速排序）
    - order: 如果数组包含字段，则是要排序的字段
- ```numpy.argsort() ``` 返回数组值从小到大的索引


# numpy.matlib
- numpy.matlib.empty(shape,dtype,order)
- numpy.matlib.empty(shape,dtype,order)
# numpy线性代数
- numpy.dot() 向量内积或矩阵乘
- numpy.vdot() 向量内积或  矩阵展开成向量再做向量内积
- numpy.matmul() 矩阵乘
- numpy.linalg.det() 求行列式值
- numpy.linalg.solve() 
- numpy.linalg.inv()
# numpy matplotlib
绘图
