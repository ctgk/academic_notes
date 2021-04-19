# Exponential distribution

## Probability density function

$$
p(x) = \begin{cases}
    \lambda e^{-\lambda x} & (x \ge 0) \\
    0 & (x < 0)
    \end{cases}
$$

where $\lambda$ is rate paramter.

## Properties

### Mean

$$
\begin{aligned}
\mathbb{E}[x] &= \int^{\infty}_0 x p(x) \mathrm{d}x\\
&= \int^{\infty}_0 x \lambda e^{-\lambda x} \mathrm{d}x\\
&= \left[-x e^{-\lambda x} - {1\over\lambda} e^{-\lambda x}\right]^{\infty}_0\\
&= {1\over\lambda}
\end{aligned}
$$

### Kullback-Leibler divergence

Kullback-Leibler divergence from $p_1(x) = \lambda_1 e^{-\lambda_1 x}$ to
$p_2(x) = \lambda_2 e^{-\lambda_2 x}$ is,

$$
\begin{aligned}
KL(p_1||p_2) &= \int p_1(x)\ln{p_1(x)\over p_2(x)}\mathrm{d}x\\
&= \int p_1(x)
    \ln{\lambda_1 e^{-\lambda_1 x}\over\lambda_2 e^{-\lambda_2 x}}\mathrm{d}x\\
&= \int p_1(x)
    \left(
        \ln{\lambda_1\over\lambda_2}
        + \ln e^{-(\lambda_1 - \lambda_2)x}
    \right)\mathrm{d}x\\
&= \ln{\lambda_1\over\lambda_2} \int p_1(x)\mathrm{d}x
    - (\lambda_1 - \lambda_2) \int x p_1(x)\mathrm{d}x\\
&= \ln{\lambda_1\over\lambda_2} - {\lambda_1 - \lambda_2 \over \lambda_1}\\
&= {\lambda_2\over\lambda_1} + \ln{\lambda_1\over\lambda_2} - 1.
\end{aligned}
$$
