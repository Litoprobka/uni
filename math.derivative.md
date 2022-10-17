---
id: 5xir3tn36aq6gg5qnrpucjc
title: Derivative
desc: ""
updated: 1665733626550
created: 1653397030371
---

Производная $f'(x)$ обозначает скорость изменения функции $f$ в точке $x$.

$$
\begin{equation}
    f'(x) = {\lim\limits_{\Delta x \to 0}} {f(x + \Delta x) - f(x) \over \Delta x}
    \end{equation}
$$

## Производные некоторых функций

$$
C' = 0 \\
x' = 1 \\
f(x) = kx + b, f'(x) = k \\
\sin' x = \cos x \\
\cos' x = -\sin x \\
(e^x)' = e^x \\
(a^x)' = a^x \ln a
\ln' x = {1 \over x} \\
(x^n)' = nx^{n-1} \\
$$

## Свойства

$$
(f + g)' = f' + g' \\
(fg)' = f'g + fg' \\
({f \over g})' = {f'g - fg' \over g^2}, g \not = 0 \\
(g \circ f)'(x) = g'(f(x)) * f'(x) \\
\exists f'(x_0) \implies f \text{ непрерывна в } x_0 \\
(f^{-1})' = {1 \over f'(f^{-1}(x))}
$$

  

### Доказательства

* $\epsilon(\Delta x) = {\Delta f(x_0) \over \Delta x} - f'(x_0) = {f(x_0+\Delta x) - f(x_0) \over \Delta x} - f'(x_0)$  
  $\lim\limits_{\Delta x \to 0}\epsilon(\Delta x) = 0, \epsilon(\Delta x) -$ бесконечно малая функция $\implies \Delta f(x_0) = f'(x_0) + \epsilon(\Delta x)\Delta x {\to \atop \Delta x \to 0} 0 \implies f(x) -$ непрерывная
* $$(Af(x)+Bg(x))' = \lim\limits_{\Delta x \to 0} {(Af(x + \Delta x) + Bg(x + \Delta x)) - (Af(x) + Bg(x)) \over \Delta x} = \lim\limits_{\Delta x \to 0} A{f(x + \Delta x) - f(x)}+B{g(x + \Delta x) - g(x)} \implies \blacksquare$$
* 
$$
(f(x)g(x))' = \lim\limits_{\Delta x \to 0}{(f(x + \Delta x)g(x + \Delta x)-f(x)g(x))+(f(g)g(x + \Delta x)-f(x)g(x)) \over \Delta x} = ...
$$
*TODO*
* 
$$
{(f(x) \over g(x))}' = \lim\limits_{\Delta x \to 0}{{f(x + \Delta x) \over g(x + \Delta x)} - {f(x) \over g(x)} \over \Delta x} = ...
$$
*TODO*
* Пусть $\exists f'(x_0), \exists x'(t_0), x(t_0)=x_0 \implies (f(x(t)))'=f'(x_0)x'(t_0)$  
$$
\Delta f(x_0) = f'(x_0)\Delta x + \epsilon(\Delta x)\Delta x \\
\text{пусть } \Delta x=x(t_0 + \Delta t) - x(t_0) \\
\Delta f(x_0)=f(x_0 + \Delta x) - f(x_0) = f(x(t_0 + \Delta t)) - f(x(t_0)) \\\implies (f(x(t)))' = \lim\limits_{\Delta t \to 0} {f(x(t_0 + \Delta t)) - f(x(t_0)) \over \Delta t} = \lim\limits_{\Delta t \to 0} {\Delta f(x_0) \over \Delta t} \\ = \lim\limits_{\Delta t \to 0} f'(x_0)*{\Delta x \over \Delta t} + \epsilon(\Delta x){\Delta x \over \Delta t} = f'(x)x'(t_0)
$$
* 
$$
f(f^{-1}(x)) = x \iff (f(f^{-1}(x)))' = x' \\
(f(f^{-1}(x)))' = 1 \\
f'(f^{-1}(x))(f^{-1}(x))' \implies (f^{-1}(x))' = {1 \over f'(f^{-1}(x))}
$$

### Примеры

* 
$$
(\tg x)' = {(\sin x)'\cos x - \sin(\cos x)' \over \cos^2 x} = {\cos^2 x + \sin^2 x \over \cos^2 x} = 1 + {\sin^2 x \over \cos^2 x}
$$
*
$$
(\arcsin x)' = {1 \over \cos(\arcsin x)} = {1 \over \sqrt{1 - \sin^2(\arcsin x)}} = {1 \over \sqrt{1 - x^2}}
$$
*
$$
(\arccos x)' = {1 \over -\sin(\arccos x)} = -{1 \over \sqrt{1 - \cos^2(\arccos x)}} = -{1 \over \sqrt {1 - x^2}}
$$
*
$$
(\arctg x)' = {1 \over 1 + \tg^2(\arctg x)} = {1 \over 1 + x^2}
$$


## Геометрический смысл

*(картинка с касательной)*  
${f(x_0+\Delta x) \over \Delta x} = \tg \alpha$, где $\alpha$ - угол наклона в точке $x_0$  
$y - f(x_0) = f'(x_0)(x-x_0)$ - уравнение касательныой к графику f(x) в точке $x_0$

---

## Гиперболические функции
$$
\sh x = {e^x-e^{-x} \over 2} \\
\ch x = {e^x + e^{-X} \over 2} \\
\th x = {e^x-e^{-x} \over e^x+e^{-x}} \\
\ch^2 x - \ch^2 x = 1 - \text{основное гиперболическое тождество} \\
\ch(x+y) = \ch x\ch y + \sh x \sh y
\sh(x+y) =\ ?
$$

### Их производные
$$
(\sh x)' = {e^x + e^{-x} \over 2} = \ch x \\
(\ch x)' = {e^X - e^{-x} \over 2} = \sh x \\
(\th x)' = {\ch^2 x + \sh^2 x \over \ch^2 x}
$$