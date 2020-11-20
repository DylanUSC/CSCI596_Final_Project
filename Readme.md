# Application of Fast multipole methods (FMM) in colloid/ionic liquid thruster simulation

Ziyu Huang

## N-body simulation of Coulomb interactions


Coulomb Interactions:

$\mathbf{f}_{i}=q_{i} \sum_{j=1 \atop j \neq i}^{N} q_{j} \frac{\mathbf{x}_{i}-\mathbf{x}_{j}}{\| \mathbf{x}_{i}-\mathbf{x}_{j}||^{3}}, \quad i=1, \ldots, N$

Direction calculation: $O(N^2)$

Barnes–Huts Tree method:

![](https://cdn.mathpix.com/snip/images/ttekX93H8f89SAWWH5_Y0BGwXbVkfrBb7nKiGceT_zM.original.fullsize.png)

![](https://cdn.mathpix.com/snip/images/iS3PsnH9W8YL5WFPQE-qfGfdXwvTjqk8k0yJnUZ9rwg.original.fullsize.png)

![](https://cdn.mathpix.com/snip/images/Mua2WcQcsTBTDkDl2Oaw-k2t7a9HAR17Bzpig-IL8uM.original.fullsize.png)



## Fast Multipole Methods:

$\phi(\mathbf{r})=\sum_{i=1}^{k} \frac{q_{i}}{\left\|\mathbf{r}-\mathbf{r}_{i}\right\|}=\sum_{n=0}^{\infty} \mathbf{M}^{\{n\}}: \mathbf{\nabla}^{\{n\}} \frac{1}{r}$ with $\mathbf{M}^{\{n\}}=\sum_{i=1}^{k}(-1)^{n} \frac{q_{i}}{n !} \mathbf{r}_{i}^{\{n\}}$


### Goal 1:

Implement parallelized FMM into our ionic liquid simulation code including injecti

### Goal 2:

Attemp to implement FMM on GPU based on  Kohnke et at JCTC, 2020.

## Reference:

Kohnke, Bartosz, Carsten Kutzner, and Helmut Grubmüller. "A GPU-accelerated Fast Multipole Method for GROMACS: performance and accuracy." Journal of Chemical Theory and Computation (2020).

