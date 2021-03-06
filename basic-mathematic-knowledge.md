# Basic Mathematic Knowledge

### 1.1 导数 \(Derivative\)

导数代表了函数岁自变量的变化速率，导数衡量的是一个变量对函数值影响能力的大小。导数&gt;0时，说明自变量\(x\)increase时，函数值\(f\(x\)\)也increase，反之相反  
常见的导函数可参考  
[ib mathematic formula book](http://edukraft.in/documents/Math HL Formulae IB.pdf).

##### 1.1.2 偏导

一般都是只有一个自变量的函数，比如f\(x\)=2x,如果自变量有多个，如何求导？比如`f=x+y`,怎样衡量x和y分别对函数值f的影响快慢呢?  
数学上引入了偏导的概念，对于一个多变量函数f，求f对其中一个自变量x的偏导很简单，就是将与x无关的其他自变量视为常亮，再使用单变量求导的方法去求导。得到的即为f对x的偏导。比如：

* 令f=x+2y, 则f对x求偏导的结果为1，对y求偏导的结果为2。
* 令f=x\*y, 则f对x求偏导结果为y，对y求偏导结果为x。

##### 1.1.3梯度

对于单变量函数，导数的正负代表自变量对函数值影响的“方向”：变大或变小。对于多变量函数，表达这个方向，使用了“梯度”（Gradient）的概念。

梯度是一个向量，向量长度与自变量的个数相等，且其中每一个元素为，函数对于对应变量求偏导的值。简单的说，就是在函数图像上，每一个变量求偏导后的到的值，这个值就是梯度。比如：

函数f=x\*y,其梯度向量为\(y,x\),因为f对于x求偏导为y，f对于y求偏导为x。带入x=1，y=1的点，其梯度向量就是\(1,1\).，带入x=10,y=-20的点，其梯度向量为\(-20,10\)

需要记忆的关键是：

* 梯度是一个向量

* **梯度指的是使函数值增大最快的方向。**在下一章中的损失函数图\(凸函数\)，梯度所指的方向是向上的

##### 1.1.4 Chain Rule 混合函数求导的链式法则

此章不需多讲，属于高中数学的知识。大体就是复合函数如：  
f\(g\(x\)\)，设g\(x\)=u,则f'\(u\)=f'\(u\)\*g'\(x\)

### 1.2 矩阵（Matrix）

一个m\*n的矩阵为一个m行n列的数组，比如：

a是一个3_2的矩阵，b是一个2_3的矩阵，c是一个3_1的矩阵，d是一个1_2的矩阵。

c只有一列，则称为**列向量**，d只有一行，则称为**行向量**

##### 1.2.1 矩阵的运算法则

1. 数乘运算

一个scalar乘以矩阵，得到的结果为矩阵中的每个元素和该scalar相乘，如下

![](/assets/scalar_martix.png)

1. 矩阵的转置运算：  
   如下，注意方向

![](/assets/zhuanzhi.png)

1. 加减法：  
   如下，矩阵之间的加减法要求尺寸相同，然后对应的元素相加减

![](/assets/plus and minues.png)

**矩阵之间的乘法,很重要，必须理解**

如下图所示，猛一看会觉得很迷茫，请记住如下口诀，带入进图看:

![](/assets/times.png)

**结果中第i行第j列的元素，等于 第一个矩阵中第i行的所有元素，与第二个矩阵中的第j列的所有元素，分别相乘后再相加**

很容易看出，矩阵乘法首先要求参数运算的两个矩阵的尺寸能fit，第一个矩阵的列数和第二个矩阵的行数必须相同，这样才能保证“第一个矩阵”中的第i行所有元素与”第二个矩阵“中第j列的所有元素可以”一一对应“。

请记住**矩阵乘法不满足交换律**交换两个矩阵位置后尺寸未必相同，即使尺寸相同结果也未必相同。

