# 第4章 曲面映射：度量

**度量**（Metric）：也被称为第一基本形式（First fundamental form），表示两个临近点之间的无穷小距离的参数化规则。
参数化的规则选取可以有很多种，因此每个曲面原则上可以写下无穷多种度量。
但是度量决定了曲面的内蕴几何，这是高斯最早对微分几何的基本见解。

例如，平面可以有无穷多种度量，直角坐标系中$d\hat{s}^{2}=dx^{2}+dy^{2}$，极坐标中是$d\hat{s}^{2}=dr^{2}+r^{2}d\theta^{2}$.
其对应的**度量张量**分别为：
$$
\begin{equation}
g=
\begin{pmatrix}
 1 & 0 \\
 0 & 1
\end{pmatrix}, \quad
g=
\begin{pmatrix}
 1 & 0 \\
 0 & r^{2}
\end{pmatrix}.
\end{equation}
$$

下面我们看球面。
我们先考虑球坐标系$(\phi, \theta)$,其中$\phi\in[0, \pi]$是极角，表示维度的取值范围；$\theta\in[0, 2\pi)$是方位角，表示经度的取值范围。

球面上的一点$(x, y, z)$可以参数化为$(R\sin\phi\cos\theta, R\sin\phi\sin\theta, R\cos\phi)$.