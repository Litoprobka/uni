---
id: 5xir3tn36aq6gg5qnrpucjc
title: Derivative
desc: ""
updated: 1666360108344
created: 1653397030371
---

Производная $f'(x)$ обозначает скорость изменения функции $f$ в точке $x$.

$$
\begin{equation}
f'(x) = {\lim\limits_{\Delta x \to 0}} {f(x + \Delta x) - f(x) \over \Delta x}
\end{equation}
$$

## Производные некоторых функций

* $C' = 0$
* $(x^n)' = nx^{n-1}$
  * $x' = 1$
  * $f(x) = kx + b, f'(x) = k$
* $(a^x)' = a^x \ln a$
  * $(e^x)' = e^x$
* $\ln' a^x = {1 \over x \ln a}$
  * $\ln' x = {1 \over x}$

### Тригонометрические функции

* $\sin' x = \cos x$
* $\cos' x = -\sin x$
* $\tg' x = {1 \over \cos^2 x}$
* $\ctg' x ={1 \over \sin^2 x}$
* $\arcsin' x = {1 \over \sqrt{1 - x^2}}$
* $\arccos' x = -{1 \over \sqrt{1 - x^2}}$
* $\arctg' x = {1 \over \sqrt{1 + x^2}}$
* $\arcctg' x = -{1 \over \sqrt{1 - x^2}}$

### Гиперболические функции

* $\sh' x = \ch x$
* $\ch' x = \sh x$
* $\th' x = {1 \over \ch^2 x}$
* $\cth' x = -{1 \over \sh^2 x}$

## Свойства

* $(f + g)' = f' + g'$
* $(fg)' = f'g + fg'$
* $({f \over g})' = {f'g - fg' \over g^2}, g \not = 0$
* $(g \circ f)'(x) = g'(f(x)) * f'(x)$
* $\exists f'(x_0) \implies f \text{ непрерывна в } x_0$
* $(f^{-1})' = {1 \over f'(f^{-1}(x))}$

### Доказательства

*$\epsilon(\Delta x) = {\Delta f(x_0) \over \Delta x} - f'(x_0) = {f(x_0+\Delta x) - f(x_0) \over \Delta x} - f'(x_0)$
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

## Логарифмическое дифференцирование

$$y = f(x) \\
\implies \ln y = \ln f(x) \\
\implies (\ln y)' = (\ln f(x))' \\
\implies {1 \over y}y' = (\ln(f(x)))' \\
\implies y' = y(\ln f(x))'$$

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

## Производные высших порядков

Пусть $\forall x \in M\ \exists f'(x)$, тогда $f'(x)$ можно рассматривать как функцию на $M$

Вторая производная $f(x) = (f'(x))'$

$n$-ная производная $f(x) = f^{(n)}(x) = (f^{n-1}(x))'$

### Примеры

* $\sin' = \cos$  
  $\sin'' = -\sin$  
  $\sin''' = -\cos$
  $\sin'''' = \sin$

## Производные параметрической функции

$$
\begin{cases}
x = \phi(t) \\
y = \psi(t)
\end{cases}\\
\begin{cases}
t = \phi^{-1}(x) \\
y = \psi(\phi^{-1}(x))
\end{cases} \\
\implies ... \implies y'(x) = {y'(t) \over x'(t)}
$$  
*TODO*

## Производная функции, заданный неявно

$(x, y) = 0$

### Пример

$$
x^2 + y^2 + \ln (3+y^2) - 10 = 0 \\  
x^2 + y^2(x) + \ln (3 + y^2(x)) - 10 = 0 \\
2x + 2y(x)y'(x) + {1 \over 3 + y^2(x)} 2y(x)y'(x) = 0 \\
2x = y'(x)(2y(x) + {1 \over 3 + y^2(x)} 2y(x)) \\
y'(x) = -{2x \over 2y + {2y \over 3 + y^2}}
$$

## Теорема о среднем

> Определение. $x_0$ - точка локального максимума (минимума) для $f(x)$ $\iff \exists U(x_0) : \forall x \in U(x_0)\ f(x_0) \geq f(x)\$ ($\leq$ для минимума, строгие неравенства для точки строгого локального минимума / максимума)

### Теорема Ферма

Пусть $x_0$ - точка локального экстремума, $\exists f'(x_0) \implies f'(x_0) = 0$

#### Доказательство

Пусть $x_0$ - локальный максимум  
Рассмотрим
${\Delta f(x_0, \Delta x)\over \Delta x} = {f(x_0 + \Delta x) - f(x) \over \Delta x} = \\
\begin{cases}
\leq 0,\ \Delta x > 0 \forall \Delta x \\
\geq 0,\ \Delta x < 0 \forall \Delta x
\end{cases}
\implies \lim\limits_{\Delta x \to +0} {\Delta f(x_0, \Delta x)} \leq 0, \lim\limits_{\Delta x \to -0} {\Delta f(x_0, \Delta x)} \geq 0 \implies \lim\limits_{\Delta x \to 0} {\Delta f(x_0, \Delta x)} = 0$

### Теорема Ролля

Пусть $f(x)$ непрерывна на $[a, b]$, дифференцируема на $(a, b)$ и $f(a) = f(b)$, тогда
$\exists c \in (a, b) : f'(c) = 0$

#### Доказательство

* ${\min \atop [a, b]} = m = M = {\max \atop [a, b]} \implies f(x) = const \implies f'(c) = 0\ \forall c \in (a, b)$
* $m \neq M \implies \exists c \in (a, b) : c - \text{локальный экстремум для } f(x) \implies f'(c) = 0 \text{ по теореме Ферма}$
