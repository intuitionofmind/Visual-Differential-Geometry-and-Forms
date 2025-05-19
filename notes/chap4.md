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

下面我们看球面的例子。
我们先考虑球坐标系$(\phi, \theta)$,其中$\phi\in[0, \pi]$是极角，表示纬度的取值范围；$\theta\in[0, 2\pi)$是方位角，表示经度的取值范围。
我们先来看几何直观。

然后，让我们详细计算。
球面上的一点$(x, y, z)$可以用球坐标参数化，即：$(x(\phi, \theta), y(\phi, \theta), z(\phi, \theta))=(R\sin\phi\cos\theta, R\sin\phi\sin\theta, R\cos\phi)$.
进一步地，球面上任意一条曲线可以用一个参数参数化，即$\mathbf{r}=\mathbf{r}(t)=\mathbf{r(\phi(t), \theta(t))}$.
其切向量为：$\mathbf{r}^{\prime}(t)=\partial_{\phi}\mathbf{r}\dot{\phi}+\partial_{\theta}\mathbf{r}\dot{\theta}$.
其中两个极坐标参数的切向量为：
$$
\begin{equation}
\begin{aligned}
\mathbf{r}_{\phi}
&=\frac{\partial\mathbf{r}}{\partial\phi}
=\left(R\cos\phi\cos\theta, R\cos\phi\sin\theta, -R\sin\phi\right), \\
\mathbf{r}_{\theta}
&=\frac{\partial\mathbf{r}}{\partial\theta}
=\left(-R\sin\phi\sin\theta, R\sin\phi\cos\theta, 0\right).
\end{aligned}
\end{equation}
$$
球面度量为
$$
\begin{equation*}
\begin{aligned}
d\hat{s}^{2}
&=dx^{2}+dy^{2}+dz^{2} \\
&=(\partial_{\phi}{x}d\phi+\partial_{\theta}{x}d\theta)^{2}+(\partial_{\phi}{y}d\phi+\partial_{\theta}{y}d\theta)^{2}+(\partial_{\phi}{z}d\phi+\partial_{\theta}{z}d\theta)^{2} \\
&=\mathbf{r}_{\phi}\cdot\mathbf{r}_{\phi}d\phi^{2}+\mathbf{r}_{\theta}\cdot\mathbf{r}_{\theta}d\theta^{2}+\mathbf{r}_{\phi}\cdot\mathbf{r}_{\theta}d\phi{d}\theta+\mathbf{r}_{\theta}\cdot\mathbf{r}_{\phi}d\theta{d}\phi.
\end{aligned}
\end{equation*}
$$
则其度量张量为
$$
\begin{equation}
g=\begin{pmatrix}
 g_{\phi\phi} & g_{\phi\theta} \\
 g_{\theta\phi} & g_{\theta\theta}
\end{pmatrix}
=\begin{pmatrix}
 \mathbf{r}_{\phi}\cdot\mathbf{r}_{\phi} & \mathbf{r}_{\phi}\cdot\mathbf{r}_{\theta} \\
 \mathbf{r}_{\theta}\cdot\mathbf{r}_{\phi} & \mathbf{r}_{\theta}\cdot\mathbf{r}_{\theta}
\end{pmatrix}
=\begin{pmatrix}
R^{2} & 0 \\
0 & R^{2}\sin^{2}\phi
\end{pmatrix}.
\end{equation}
$$
最终，球面用$(\phi, \theta)$写下的度量为$d\hat{s}^{2}=R^{2}\left(d\phi^{2}+\sin^{2}\phi{d}\theta^{2}\right)$.