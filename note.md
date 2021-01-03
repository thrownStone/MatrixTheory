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

- 第一范数 
- 第二范数 
- 无穷范数
- holder不等式

### matrix norm：

- 1范数
- 2范数（tr(A^H*A)）
- 无穷范数
- 算子范数
- 谱范数（sqrt(r(A^H*A))）

### 常用不等式：

- 三角不等式
- 向量内积不等式及相关变体（个人理解）

### Problem Set：

	1. y = Bx （8）
	
# chapter 3

对称矩阵：

- egienvector正交，且可以选出orthornomal egienvector
- 实对称矩阵egienvalue均为实数
- 可对角化为 QλQ^T

Hermite矩阵：

- eigenvalue为实数
- 可对角化

Unitary矩阵：

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

- A = U * (R; O)
- A = (L O) * U
- A = U * R（唯一）
- A = L * U（唯一）
- A = U * (L O; O O) * V

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
- Schur定理：A = URU^H （A属于C^n*n，R中主对角元为A的eigenvalue）
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

### Problem Set：

需要重做

# chapter 4

## 4.1

### Schur不等式

### Hirsch不等式

### Bendixson不等式&推论

### Browne不等式

### Hadamard不等式

## 4.2

### 圆盘定理

### 圆盘定理1

### 圆盘定理2

### 推论

- 1
- 2
- 3
- 4

### 定理3

### 定理4

## 4.3

### Rayleigh Quotient

### 

### 

### 

### 

### 

### 
