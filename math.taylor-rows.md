---
id: 3vn8heqiqmxpk2jkt8np3yw
title: Taylor Rows
desc: ''
updated: 1668262733282
created: 1666940521079
---

## Многочлен Тейлора

$P(x) = \displaystyle\sum_{i = 0}^n a_ix^i = \displaystyle\sum_{i = 0}^n b_i(x - x_0)^i$

* $P(x_0) = b_0, P'(x) = b_1 + 2b_2(x-x_0) + 3b_3(x-x_0)^2 + \dots + nb_n(x - x_0)^{n - 1}$  
* $P'(x_0) = b_2$  
* $P''(x_0) = 2b_2 + 3 * 2(x - x_0) + \dots + n(n-1)b_n(x-x_0)^{n-2}$  
* $P'''(x_0) = 3!b_3$  
* $\dots$  
* $P^{(n)}(x_0) = n!b_n$

$P(x) = \displaystyle\sum_{k = 0}^n a_kx^k = \displaystyle\sum_{k = 0}^n {P^{(k)}(x_0) \over k!}(x - x_0)^k$

> Пусть $f(x)$ произвольная, $n$ раз дифференцируемая в точке $x_0$ функция. многочленом Тейлора степени $n$ функции $f(x)$ в точке $x_0$ называется многочлен
> $$
> Q_n = \displaystyle\sum_{k = 0}^n {f^{(k)}(x_0) \over k!}(x - x_0)^k$$

### Теорема Тейлора

Пусть $f(x)$ имеет $(n+1)$-ую непрерывную производную в $u(x_0)$, тогда $\forall x \in u(x_0), \exists \theta_x \in (x_0, x)$:

$$
f(x) = \displaystyle\sum_{k=0}^n {f^{(k)}(x_0) \over k!}(x - x_0)^k + {f^{(n+1)}(\theta_x) \over (n+1)!}(x - x_0)^{n + 1}
$$

Пусть $Q_n(x) -$ многочлен Тейлора для $f(x)$.

* $Q_n(x_0) = f(x_0)$
* $Q'_n(x_0) = f'(x_0)$
* $\dots$
* $Q^{(n)}_n(x_0) = f^{(n)}(x_0)$

$f(x)=Q_n(x) + r_n(x),$ где $r_n(x) = f(x) - Q_n(x)$ - остаточный член разложения Тейлора степени $n$.

$\omega_n(x) = (x - x_0)^{n + 1}$

${r_n(x) \over \omega_n(x)} = {r_n(x) - r_n(x_0) \over \omega_n(x) - \omega_n(x_0)} = {r'_n(x_1) \over \omega'_n(x_1)} = {r'_n(x_1) - r'_n(x_0) \over \omega'_n(x) - \omega'_n(x_0)} = \dots = {r^{(n)}(x_n) \over \omega^{(n)}(x_n)} = {r^{(n+1)}(x_{n+1}) \over \omega^{(n + 1)}(x_{n+1})} = {f^{(n + 1)}(x_{n+1}) \over (n+1)!}$

$$
{f^{(n + 1)}(x_{n+1}) \over (n+1)!} = {r_n(x) \over (x - x_0)^{n + 1}}
$$
