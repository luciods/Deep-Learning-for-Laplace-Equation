# Deep-Learning-for-Laplace-Equation
The universal approximation theorem guarantees the power of neural networks to approximate any function. This means solving partial differential equation too. 
In the simplest construction of the network, the solution $u(t,x)$ is given by $u(t,x)\simeq nn(t,x;\theta)$ where $nn(t,x;\theta)$ is the output and $\theta$ are the parameters that minimize best the loss function $$J(\theta)=\dfrac{1}{|\Omega||[0,T]|}\sum_{(t_i,x_i)\in [0,T]\times \Omega}\left(\hat{\mathcal{L}}nn(t_i,x_i;\theta)-f(t_i,x_i)\right)^2+J_{IC}+J_{B}$$ where $\hat{\mathcal{L}}$ is the differential operator and $IC$ and $B$ are the initial and boundary conditions respectively. As an optimization problem, the possiblity of getting stuck into some local minimum is not negligible. An improvement could be the 'weighting' of the loss function, for example $J(\theta)=p_1 J_{\mathcal{L}}+p_2 J_{IC}+p_3 J_{B}$ with $p_1+p_2+p_3=1$, in order to force the optimizer to give higher account to some terms of the loss function. Another powerful way to improve the convergence is the construction of the solution in order to automatically satisfies initial and boundary conditions. Such minimization problem is called unconstrained, since the only term to be minimized is the differential equation.


## References
[https://arxiv.org/abs/1711.06464]
