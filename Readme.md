# Application of Fast multipole methods (FMM) in colloid/ionic liquid thruster simulation

Ziyu Huang

## N-body simulation of Coulomb interactions


Coulomb Interactions:



![](https://latex.codecogs.com/svg.latex?\begin{equation}\mathbf{f}_{i}=q_{i}%20\sum_{j=1%20\atop%20j%20\neq%20i}^{N}%20q_{j}%20\frac{\mathbf{x}_{i}-\mathbf{x}_{j}}{\left\|\mathbf{x}_{i}-\mathbf{x}_{j}\right\|^{3}},%20\quad%20i=1,%20\ldots,%20N\end{equation})

Direction calculation: $O(N^2)$

Barnes–Huts Tree method:

![](https://cdn.mathpix.com/snip/images/ttekX93H8f89SAWWH5_Y0BGwXbVkfrBb7nKiGceT_zM.original.fullsize.png)

![](https://cdn.mathpix.com/snip/images/iS3PsnH9W8YL5WFPQE-qfGfdXwvTjqk8k0yJnUZ9rwg.original.fullsize.png)

![](https://cdn.mathpix.com/snip/images/Mua2WcQcsTBTDkDl2Oaw-k2t7a9HAR17Bzpig-IL8uM.original.fullsize.png)



## Fast Multipole Methods:

$\phi(\mathbf{r})=\sum_{i=1}^{k} \frac{q_{i}}{\left\|\mathbf{r}-\mathbf{r}_{i}\right\|}=\sum_{n=0}^{\infty} \mathbf{M}^{\{n\}}: \mathbf{\nabla}^{\{n\}} \frac{1}{r}$ with $\mathbf{M}^{\{n\}}=\sum_{i=1}^{k}(-1)^{n} \frac{q_{i}}{n !} \mathbf{r}_{i}^{\{n\}}$


### Attempt 1:

Implement parallelized FMM into our ionic liquid simulation code including injecti

### Attempt 2:

Attemp to implement FMM on GPU based on  Kohnke et at JCTC, 2020.

### Attempt 3:

Vectorisation (Pfalzner and Gibbon 2005)

![](https://cdn.mathpix.com/snip/images/CzwPWY26QGvEW49hBqQBBeJropclgY2Rtvrop1jCo5I.original.fullsize.png)

## Reference:

[1] Kohnke, Bartosz, Carsten Kutzner, and Helmut Grubmüller. "A GPU-accelerated Fast Multipole Method for GROMACS: performance and accuracy." Journal of Chemical Theory and Computation (2020).

[2] Pfalzner, Susanne, and Paul Gibbon. Many-body tree methods in physics. Cambridge University Press, 2005.

