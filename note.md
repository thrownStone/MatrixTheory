# chapter 1

Jordan form

用来解决eigenvector几何重数小于代数重数的问题。设方阵为n * n，只有s个eigenvector。那么，Jordan form中有s个Jordan block，每个Jordan block的形式是：对角线为eigenvalue，上方为1。

投影矩阵：满足幂等

正交投影：满足幂等且为Hermitian矩阵

# chapter 2

### norm property：

- 正定（非负）
- 齐次
- 三角不等式


### vector norm： 

- 1范数 
- 2范数 
- 无穷范数
- holder不等式
- Vn(P)上任意向量范数是等价的

### matrix norm：

- 1范数
- 2范数（tr(A^H*A)）
- 无穷范数
- 算子范数（与向量相容矩阵范数中最小者）
- 谱范数（sqrt(r(A^H*A))）
- P^m*n上的任意矩阵范数等价

### 常用不等式：

- 三角不等式
- 向量内积不等式及相关变体（个人理解）

### Problem Set：

	1. y = Bx （8）
	
# chapter 3

### 对称矩阵：

- egienvector正交，且可以选出orthornomal egienvector
- 实对称矩阵egienvalue均为实数
- 可对角化为 QλQ^T

### Hermite矩阵：

- eigenvalue为实数
- 可对角化

### Unitary矩阵：

- 特征值模为1

实正定矩阵：

- 所有特征值大于0
- 可分解为A^T*A，其中A为可逆矩阵

正三角矩阵的前提是方阵

### A为满秩方阵时唯一分解：

- A = UR (QR)
- A = LU (LQ)
- A = R^H*R (正定)
- A = R^T*R (正定)

### A为任意矩阵时分解:

- A = U * (R; O) （行满秩）
- A = (L O) * U（列满秩）
- A = U * R（唯一）（行满秩）
- A = L * U（唯一）（列满秩）
- A = U * (L O; O O) * V
- Schur定理：A = URU^H （A为方阵，R中主对角元为A的eigenvalue）

唯一分解的直观解释：基向量的数量（即空间维度） = 矩阵的rank（即无关向量个数）

### 谱分解：

- 单纯矩阵：特征值的代数重复度与几何重复度相同
- 单纯矩阵谱分解Ai性质：幂等、分离、可加（直接相加为E，加权相加为A）
- 单纯矩阵的充要条件（有k个不同的特征值时）：分离、可加

### Hermite矩阵分解

常用的还是A = U * λ * U^H

### 正规矩阵

- 正规矩阵：A^H * A = A * A^H
- U相似：A = UBU^H
- U等价：A = UBV
- 正规矩阵A与矩阵B U相似，则B也是正规矩阵
- 三角矩阵A是正规矩阵的充要条件：A是对角矩阵
- A是正规矩阵的充要条件：A = U * diag( eigenvalue ) * U^H or A有k个不同特征值，且A同时是Hermite矩阵和单纯矩阵

### 最大秩分解

A = BD

B列满秩

D行满秩

注意计算方法

### SVD 

特征值对角化的不足：

	The eigenvectors in X have three big problems: 
	1. They are usually not orthogonal, there are not always enough eigenvectors, 
	2. Ax = lambda * x requires A to be a square matrix. 
	The singular vectors of A solve all those problems in a perfect way

 由此引入了SVD
	A = U * Σ * V^H

其中，Σ是奇异值矩阵，σ = sqrt(λ(A^T * A))

引入：

	A: m * n
	u 是属于R^n的orthonormal basis
	v 是属于R^m的orthonormal basis
	若v u之间满足：Av_i = σ_i * u_i，则可得到AV = UΣ --> A = UΣV^H

Proof:

	A^T * A = V (Σ^T * Σ) V^H
	所以，V是A^TA的eigenvector，eigenvalue是σ^2
	又因为Av_i = σ_i * u_i，可以证明u之间满足正交的关系。事实上，u是AA^H的eigenvector。（A^HA AA^H的eigenvalue相同

定理1：

- rank(A) = rank(A^HA) = rank(AA^H)
- A^HA AA^H eigenvalue 非负实数
- A^HA AA^H非零特征值相同且代数重复度相同

### Problem Set：

需要重做

# chapter 4

## 4.1

### Schur不等式
矩阵特征值模的平方和 <= 矩阵的2范数 （当为正定矩阵时取等

### Hirsch不等式
A: n * n

B: (A + A^H) / 2 (Hermite)

C: (A - A^H) / 2 (anti Hermite)

- |λi| ≤ n max|a_ij|
- |Re(λi)| ≤ n max|b_ij|
- |Im(λi)| ≤ n max|c_ij|

### Bendixson不等式&推论
	|Im(λi)| ≤ sqrt(n(n-1) / 2) max|c_ij|

- 实方阵的复特征值成对出现
- Hermite矩阵的eigenvalue均为实数
- Anti Hermite矩阵的eigenvalue均为虚数

### Browne不等式
	σ_n ≤ |λi| ≤ σ_1

### Hadamard不等式

## 4.2


### 圆盘定理1

### 圆盘定理2
n个圆盘并形成一个连通区域，且与剩下的不相交才可以使用该定理 

### 推论

- 1. 行圆盘定理适用于列
- 2. all eigenvalue 都落在行、列圆盘的交集区域
- 3. n个圆盘互不相交，A相似于对角矩阵
- 4. n个圆盘互不相交，A的eigenvalue全为实数

### 定理3

### 定理4
严格对角占优有：

- A可逆
- 若A为Hermite且所有对角元为正，则A的eigenvalue均为正数

## 4.4

### Rayleigh Quotient

### C-F定理
Hermite矩阵，最大最小Rayleigh Quotient = λ_k

### Weyl定理
Hermite矩阵，矩阵特征值和的大小关系

### 推论
Hermite矩阵，且B为半正定时，特征值和的关系

## 4.5

### 单调范数

### Problem Set：

需要重做

# chapter5

## 5.1
### 序列极限性质
- 线性
- 可与乘法交换顺序
- 可与求逆交换顺序

### 序列收敛充要条件
	lim k->∞ { || A^(k) - A || = 0 }
### 收敛矩阵
	lim k->∞ { A^k = 0 }

充要条件：
	r(A) < 1
	
### 矩阵级数

- 绝对收敛的充要条件：|| A^(k) ||绝对收敛
- Neumann定理 

		sum k = 0->∞ {A^k} = I + A + A^2 + ... + A^n 收敛的充要条件是r(A) < 1，且和为(I - A)^-1

## 5.2
### 矩阵函数
常用函数级数

### 矩阵函数值计算
相似对角化：

- 特征值
- Jordan form

### 相关性质
- if AB = BA, then exp(A) * exp(B) = exp(B) * exp(A) = exp(A + B)
- if AB = BA, then cos(A + B) sin(A + B)均为三角函数展开
# chapter 6

## 6.1 单边逆

### 左可逆
列满秩
### 右可逆
行满秩
### 单边逆计算方法

## 6.2 广义逆
AGA = A
### 性质
- rank(A-) >= rank(A)
- 单边逆可以与转置、H交换运算顺序
- AA- A-A均为幂等矩阵，且rank(A) = rank(AA-) = rank(A-A)
- R(AA-) = R(A)，N(A-A) = N(A)

## 6.3 自反广义逆
	AGA = A
	GAG = G
### 性质
- Z = XAY，其中X、Y均为A的广义逆，则Z是A的自反广义逆
- A-是A的自反广义逆的充要条件：rank(A) = rank(A-) (满足GAG = G)

## 6.5 A+
	AGA = A
	GAG = G
	(AG)^H = AG
	(GA)^H = GA
### 性质
- 最大秩分解得到的A+通式
- A+是唯一的
- (A+)+ = A
- 运算顺序可与T、H交换
- (A^HA)+ = A+ * (A^H)+
- (AA^H)+ = (A^H)+ * A+
- A+ = (A^HA)+ * A^H = A^H * (A^HA)+
- R(A+) = R(A^H), N(A+) = N(A^H)
- R(A) = R(A^H) <=> AA+ = A+ * A
- R(A+A) = R(A+) = R(A^H) R(AA+) = R(A)
- AA+是R(A)的正交投影矩阵 A+A是R(A^H)的正交投影矩阵
- (AB)+ = B+A+ <=> R(A^HAB)属于R(B) R(BB^HA^H)属于R(A^H)

## 6.5 A+计算方法
### 最大秩分解
- 行满秩
- 列满秩
### SVD计算
A+的奇异值是A奇异值平方的倒数，故：

- 矩阵2范数：A奇异值倒数平方之和
- 矩阵算子范数：A最小奇异值的倒数
- (AA^H)+ = U1 * D * U1^H，其中，D为AA^H特征值矩阵的逆矩阵，U1为对应的特征向量

## 6.7 应用
### 有解及通解条件
特别注意Ax=b
### 最小二乘及最佳解
- 通解
- A+b最小范数解

