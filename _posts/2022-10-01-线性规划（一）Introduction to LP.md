# Introduction to LP

——线性规划好，方老师好

给定如下问题：
$$
\min f\left(\vec{\bold{x}}\right) \\
s.t.\ 
\begin{equation*}
	\begin{cases}
		G_1\left(\vec{\bold{x}}\right) & \ge 0 \\
		G_2\left(\vec{\bold{x}}\right) & \ge 0 \\
		\quad \vdots & \vdots \\
		G_n\left(\vec{\bold{x}}\right) & \ge 0 \\
		x_1, \cdots, x_n &\ge 0
	\end{cases}
\end{equation*}
$$
$f\left(\cdot\right)\ \ G_i\left(\cdot\right)$ is a linear function.

**How to study linear programming**

* Geometric intuition
* Algebraic manipulation
* Computer programming

**Standard Form**
$$
\min \bold{c}^{T}\bold{x} \\
s.t.\ 
\begin{array}{rl}
	\bold{A}\bold{x} &= \bold{b}\\
	\bold{x} &\ge 0
\end{array}\\
feasible\ domain: P=\left\{x\in R^n\mid\bold{A}\bold{x} = \bold{b},\ x\ge0 \right\}
$$
$\bold{A}$是$m\times n$的矩阵，$c$和$x$是n维列向量，$b$是m维列向量。A称为约束矩阵，b称为右手边向量，c称为成本向量。假定b中每一元素均为非负数。

**Converting to Standard Form**

1. 无约束变量
   $$
   x = x^{+} - x^{-},\ \left|x\right| = x^{+} + x^{-} \\
   \begin{equation}
   	x^{+} = \left\{
   	\begin{array}{cc}
   		x, & x > 0 \\
   		0, & x \leq 0
   	\end{array}\right.
   	,\quad 
   	x^{-} = \left\{
   	\begin{array}{cc}
   		0, & x > 0 \\
   		-x, & x \leq 0
   	\end{array}\right.
   \end{equation}
   \\
   即\ \ x^{+} \ge 0,\ x^{-} \ge 0,\ x^{+} \times x^{-} = 0
   $$
   注意：$\ x^{+} \times x^{-} = 0$是一个二次约束

2. 不等式转换为等式

   * 对于$G_i\left(x\right) \leq b_i$可以通过添加变量$s_i \ge 0$构成$G_i\left(x\right)+s_i=b_i$
   * 对于$G_j\left(x\right) \ge b_j$可以通过添加变量$s_j \ge 0$构成$G_j\left(x\right)-s_j=b_j$

3. 极大极小转换（取负号）

------

# Geometry of LP

你认为一个标准线性规划的问题，解的可能情况有几种？

1. 无解
2. 有最小值
3. 负无穷