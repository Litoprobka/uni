---
id: mxp3xpf0y85pqgnrxsqpc6n
title: Дифференциальное исчисление функций нескольких вещественных переменных
desc: ''
updated: 1670569651827
created: 1668755902077
---
*нам объясняют линейные пространства. Зачем?*
$\R^n = \lbrace (x_1, x_2, \dots, x_n) : x_i \in \R\ \forall i \rbrace$

## Точки

$\lbrace M(x_1, x_2, \dots, x_n) \rbrace$

## Векторы

* $\lbrace \overrightarrow{AB} = (x_1 - x_1^0, x_2 - x_2^0, \dots, x_n - x_n^0) : B(x_1, \dots, x_n), A(x_1^0, \dots, x_n^0) \rbrace$
* $\text{Два вектора считаются равными, если все их координаты совпадают}$
* $\vec a + \vec b = (a_1 + b_1, a_2 + b_2, \dots, a_n + b_n)$
$* \lambda\vec a = (\lambda a_1, \lambda a_2, \dots, \lambda a_n) \implies \lambda \vec a + \lambda \vec b = \lambda (\vec a + \vec b); (\lambda + \mu) \vec a = \lambda \vec a + \mu \vec a$
* $\vec a \vec b = \displaystyle\sum_{i = 0}^n a_ib_i$  
  $|\vec a| = \sqrt{\vec a^2} = \sqrt{a_1^2 + a_2^2 + \dots + a_i^2}$  
  $\rho(A, B) = |AB|$  
  $|\vec a + \vec b| \leq |\vec a| + |\vec b|$
  * $\vec a^2 = \vec a \vec a \geq 0$  
  * $\vec a \vec b = \vec b \vec a$  
  * $\vec a(\vec b + \vec c) = \vec a \vec b + \vec a \vec c$

### Неравенство Коши-Бунековского

$\vec a \vec b \leq |\vec a| |\vec b|$
$$
\forall c \in \R^n\ |\vec c|^2 \geq 0 \\
\text{Рассмотрим } \vec a + t \vec b, t \in \R \\
|\vec a + t\vec b|^2 = (\vec a + t\vec b)(\vec a + t\vec b) = \vec a^2 + 2t\vec a\vec b + t^2 b^2 \geq 0\ \forall t \in \R \\
D = (2\vec a \vec b)^2 - 4\vec a^2 \vec b^2 \leq 0 \iff 4(\vec a \vec b)^2 \leq 4|\vec a||\vec b| \\
\implies |\vec a \vec b| \leq |\vec a||\vec b|
$$

### Неравенство треугольника

$\forall \vec a, \vec b \in \R^n\ |\vec a + \vec b| \leq |\vec a| + |\vec b|$
$$
|\vec a + \vec b|^2 = (\vec a + \vec b)^2 = \vec a^2 + 2\vec a\vec b + \vec b^2 = |\vec a|^2 + 2 \vec a \vec b + |\vec b|^2 \leq |\vec a|^2 + 2 |\vec a||\vec b| + |\vec b|^2 = (|\vec a| + |\vec b|)^2 \implies |\vec a + \vec b| \leq |\vec a| + |\vec b|
$$

## Окрестность

Открытым шаром радиуса $R$ с центром $A(x_i^0)$ называется множество $u_R(A) = \lbrace \sum (x_i - x_i^0) < R \rbrace$

Окрестностью точки $A$ называется произвольное множество $u(A) : \exists R > 0, u_R(A) \subset u(A)$

$\epsilon$-окрестность точки $A = u_\epsilon(A)$

Пусть $\lbrace X_n \rbrace$ - некоторая последовательность точек, $\forall i\ X_i \in \R^n$  
Точка $B \in \R^n$ - предел последовательности $\lbrace X_n \rbrace$ при $x \to \infty$, если $\forall \epsilon > 0\ \exists N_\epsilon \in \N : \forall n > N_\epsilon\ X_n \in u_\epsilon(B) \iff |\vec X_n - \vec B| < \epsilon$  
$\forall u(B)\ \exists N_{u(B)} \in \N : \forall n > N_{u(B)}\ X_n \in u(B)$$

---
Существует предел для последовательности точек $\iff$ существуют пределы для всех координат (лень нормально записывать)

## Теорема

Если $\exists \lim\limits_{k \to \infty} X_k = B$, то $\exists! \lim\limits_{k \to \infty} X_k$

Пусть существуют пределы $B$ и $B_1$
$$
\forall k > \max \lbrace N_{1\epsilon}, N_{2\epsilon} \rbrace\ |X_k - B_1| + |X_k - B| < 2d/3 \\
\text{someting неравенство треугольника something}
$$

## Теорема об ограниченности

Если $\exists \lim\limits_{k \to \infty} = B$, то $\lbrace X_n \rbrace$ - ограниченная ($\forall k\ \exists m > 0 : |X_k| < m$)

*TODO: доказательство*

## Теорема Больцано-Вейерштрасса

Из всякой ограниченной последовательности можно выделить последовательность, для которой существует предел

Пусть $\lbrace X_k \in \R^n \rbrace$ ограничена. Тогда $\exists X_{k_l} \subset \lbrace X_k \rbrace : \exists \lim\limits_{l \to \infty} X_{k_l} = B, B \in R^n$

### Доказательство

Пусть $X_k(X_{ki})$, т.к. $X_k$ - ограниченная $\implies$ $X_{k_l}$ - ограниченная. Тогда по Т. Больцано-Вейерштрасса для числовых последовательностей $\exists \lbrace x_{k_l1} \rbrace \subset \lbrace X_{k1} \rbrace : \lim\limits_{l \to \infty} X_{k_l1} = X_{01}$; выбираем в ней подпоследовательность для второй координаты, rinse and repeat

## Последовательность Коши

$\lbrace X_k \in \R^n \rbrace$ - последовательность Коши $\iff \forall \epsilon > 0 : \exists N_\epsilon \in \N : \forall k, l > N_\epsilon\ |X_k - X_l| < \epsilon$

> У последовательности сущиствует предел $\iff$ это последовательность Коши

## Открытое и закрытое множество

TL;DR ограниченное открытое множество - обобщение интервала, ограниченное замкнутое - обобщение отрезка

> Множество $M \subset R^n$ - открытое, если $\forall A \in M\ \exists u_\epsilon(A) : u_\epsilon(A) \subset M$

> Множество $G \subset \R^n$ - замкнутое $\iff CG$ (дополнение множества $G, CG = \lbrace x \in R^n : x \notin G \rbrace$) открытoe

*TODO*: доказать, что:

* $\bigcap$ конечного числа открытых множеств открытое
* $\bigcup$ любого числа открытых множеств открыто
* $\bigcap$ любого числа замкнутых множеств замкнуто
* $\bigcup$ конечного числа замкнутых множеств замкнуто

> Точка $X \in G$ - внутренняя точка $G \iff \exists u_\epsilon(X) \subset G$  
> $\dot G$ - множество всех внутренних точек  
> $\dot G$ - открытое множество; $G$ - открытое $\iff G = \dot G$

> Граница множества $G$ - $ГG = \lbrace x \in R^n : \forall u_\epsilon(X) \not \sqcap G, u_\epsilon(X) \not \sqcap CG \rbrace$  
> Теорема. $R^n = \dot G \cup ГG \cup C\dot G$

Пусть $G \subset R^n, X \in G$:

* $X \in \dot G$
* $X \in C \dot G$
* $X \in ГG$

### Замыкание множества

Замыканиеm множества $G \subset R^n$ называется $\overline G$ - минимальное замкнутое надмножество $G$ ($G \subset \overline G$)

Теорема. $\overline G = G \cup ГG$  
Доказательство.

* $G \cup ГG = \dot G \cup ГG, \dot G \cup ГG$ - замкнутое
* $\forall X \in ГG\ X \in \overline G$. От противного:  
  $X \in ГG, X \notin \overline G \implies X \in C \overline G, C \overline G$ - открытое; но $\forall u_\epsilon(X) \not \sqcap G u_\epsilon(X) \not \sqcap C \overline G \implies ?! \implies \overline G \in G \cup ГG$

### Второе определение замкнутого множества

Множество $G$ - замкнутое $\iff \forall (\lbrace X_k \rbrace : \forall k\ X_k \in G \land \exists \lim\limits_{k \to \infty} X_k = X_0)\ X_0 \in G$

Доказательство.  
Пусть $\lbrace X_k \rbrace : X_k \in g, \forall k \land \exists \lim\limits_{k \to \infty} X_k = X_0)$  
Пусть $X_0 \notin G \implies X_0 \in CG$  
Заметим, что любая $\forall u_\epsilon(X_0) \not\sqcap \lbrace X_k \rbrace \implies \nexists u_\epsilon(X_0) \subset CG$

Докажем, что $\forall x \in ГG\ x \in G$.
$\forall n \in \N\ u_{1/n}(X_0) \ni X_k$. Имеем последовательность $\lbrace X_k \rbrace : \forall X_k \in G \land \exists\lim\limits_{k \to \infty} X_k = X_0 \implies X_0 \in G \implies G \supset ГG \implies G -$ замкнутое

#### Открытое покрытие

Пусть $R = \lbrace W_\alpha \rbrace, \alpha \in I$, где $W_\alpha$ - открытое множество. $R$ называется открытым покрытием множества $G \in R^n \iff G \subset \bigcup W_\alpha$

### Ограниченное замкнутое множество

Пусть $G$ - ограниченное замкнутое множество, $R$ - некоторое покрытие $G$ открытыми множествами. Тогда $\exists d_R \in \R, d_R > 0 : \forall X \in G\ \exists \alpha \in I : u_{d_R} \subset W_\alpha$

Доказательство.
От противного, пусть $\nexists d_R \implies \forall d = 1/n\ \exists X_n \in G : u_{1 \over n}(X_n) \not\subset W_\alpha \forall \alpha \in I$. Тогда имеем $\lbrace X_n \rbrace$ - ограниченная (теорема Больцано-Вейерштрасса) $\implies \exists \lbrace X_{n_k} \rbrace \subset \lbrace X_n \rbrace : \exists \lim\limits_{k \to \infty} X_{n_k} = X_0$. Tогда $X_0 \in G$ (т.к $G$ - замкнутое) $\implies \exists \alpha_0 : X_0 \in W_{\alpha_0} \implies \exists \Delta_0 : u_{\delta_0}(X_0) \subset W_{\alpha_0}$. Заметим, что $u_{\Delta_0 \over 3}(X_0)$ содержит бесконечное чесло членов последовательности $X_{n_k}$, в частности $\exists X_{n_{k_0}} \in u_{\Delta_0 \over 3}(X_0) : u_{1 \over n_{k_0}}(X_{n_{k_0}}) \notin W_\alpha \forall \alpha \in I$, причём ${1 \over n_{k_0}} < {\Delta_0 \over 3}$

*WTF*

Теорема 2. Пусть $G$ - ограниченное замкнутое множество, $G \subset \bigcup W_\alpha$ - открытое покрытие $G$. Тогда существует конечное подмножество $I_0 \subset I : G \in \displaystyle\bigcup_{\alpha \in I_0} W_\alpha$

Доказательство. Пусть $R = \bigcup W_\alpha$ - покрытие, тогда по т.1. $\exists d > 0 : \forall x \in G\ \exists d_X : u_d(X) \subset W_{\alpha x}$

## Предел функции

$f : \R^n \to \R$  

> Определение по Гейне. Число $A$ называется пределом функции $f(X)$ при $X \to X_0 \in R^n$, если $\forall \lbrace X_n\rbrace : \exists \lim\limits_{n \to \infty} X_n = X_0\quad \exists\lim\limits_{n \to \infty} f(X_n)=A$

> Определение по Коши. Числ $A$ - предел функции $f(X)$ при $X \to X_0 \in R^n$, если $\forall \epsilon > 0\ \exists \Delta > 0 : \forall X \in \dot u_{\delta_\epsilon}(X_0)\ f(x) \in u_\epsilon(A)$

### Эквивалентность определений

"Доказательство такое же, с точностью до размера букв" - Прохоров
![[math.function.limit#теорема-об-эквивалентности-определений]].

### Свойства

(опять всё то же самое)

* существование верхней границы
* предел суммы/разности/произведения/отношения равен $\dots$ пределов
* третье свойство, которое тоже работает как у пределов функций одного аргумента

### Предел по направлению

Пусть $\vec a$ - произовольный вектор. Рассмотрим $f(X + t\vec a) = f(x_1 + ta_1, x_2 + ta_2 + \dots)$. Рассмотрим $\lim\limits_{t \to +0} f(X + t\vec a)$ - предел по направлению вектора $\vec a$

Существует предел $\implies$ существует предел по направлению, но обратное не всегда верно.

## Неприрывность

$f(X)$ - непрерывна в $X_0 \iff \exists \lim\limits_{X \to X_0} f(X) = f(X_0)$

Непрерывность сохраняется при сложении / вычитании / умножении / делениии непрерывных функций

### Непрерывность композиции

Пусть $f(X)$ непрерывна в $X_0$, $f(X_0) = t_0$, $g(t)$ непрерывна в $t_0$, тогда $(g \circ f)(X)$ непрерывна в $X_0$

#### Доказательство

$$
\lim_\limits_{\Delta x \to \infty} \Delta(g \circ f)(X_0) = \lim\limits_{\Delta X \to \infty} (g \circ f)(X_0 + \Delta X) - (g \circ f)(X_0) =
\begin{cases}
f(X_0 + \Delta X) - f(X_0) = {\Delta f(X_0) \to 0 \atop \Delta x \to 0} \\
f(X_0 + \Delta X) = f(X_0) + \Delta f(X_0) = t_0 + \Delta f
\end{cases}
$$

### Непрерывность на ограниченном замкнутом множестве

Такое же определение, как и для функции одного аргумента и отрезка

---

> $\lim\limits_{X \to \infty} f(X) = А \iff \forall \epsilon > 0\ \exists (M_\epsilon > 0 : |X| > M)\ |f(X) - A| < \epsilon$

> $\lim\limits_{X \to X_0} f(X)$ равен $\infty \iff \forall M>0\ \exists \delta_M>0 : (\forall x \in u_{\delta_M}(X_0))\ |f(X)| > M$

---

Верхняя и нижняя грань работают так же, как и с функциями одной переменной...

### Линейная связность

> Непрерывной кривой в $R^n$ называется $\Gamma : [a, b] \to \R^n$, где все координаты непрерывны (и её образ)

Множество $M \subset R^n$ - линейно связное $\iff \forall A, B \in M\ \exists \Gamma : [a, b] \to R^n : \Gamma(a) = A, \Gamma(b) = B, \forall t \in [a, b]\ \Gamma(t) \in M$

### Теорема о промежуточных значениях

*Наконец-то что-то отличается?*

### Замечание

Пусть $f(X) : \R^n \to R, f(X)$ - непрерывна, тогда множество $S = \lbrace X \in \R^n : f(X) = 0\rbrace$ - замкнуто

### Теорема Кантора

Пусть $f(X)$ непрерывна на $M$, где $M$ - ограниченное замкнутое множество. Тогда $f(X)$ равномерно непрерывна на $М$ 

---

## Частные производные

> Частная производная $f(X)$ по $x_i$ в точке $X(x_{10}, x_{20}, \dots, x_{n0}) =
\lim\limits_{\Delta \to 0}$ ${f(x_{10}, x_{20}, \dots, x_{i}+\Delta x, x_{i+1\,0}, \dots, x_{n_}) - f(X_0) \over \Delta x} = {\delta f(X_0) \over \delta x_i}$

Геометрический смысл для $\R^2$ - тангенс угла наклона касательной при фиксированном $x$ или $y$
$$
f(x_0, y) \leadsto z = f(x_0, y_0) + {\delta f \over \delta y}(x_0, y_0)(y-y_0) \\
f(x, y_0) \leadsto z = f(x_0, y_0) + {\delta f \over \delta x}(x_0, y_0)(x-x_0) \\
\text{касательная плоскость } Z = f(x_0, y_0) + {\delta f \over \delta x}(X_0)(x-x_0) + {\delta f \over \delta y}(X_0)(y-y_0)
$$

### Вторая частная производная

$$
{\delta \over \delta x}({\delta f \over \delta x}) = {\delta^2 f \over \delta x^2}
$$

### Частные производные можно брать в любом порядке

> $f(x, y)$ в окрестности $X_0$ имеет неприрывные частные производные второго порядка ${\delta^2 f \over \delta x \delta y}$ и ${\delta^2 f \over \delta y \delta x} \implies$ они равны

Рассмотрим $h_f(X_0, \Delta X) = f(x_0 + \delta x, y_0 + \delta y) - f(x_0, y_0 + \Delta y) - f(x_0 + \Delta x, y_0) + f(x_0, y_0) = (f(x_0 + \Delta x, y_0) - f(x_0, y_0 + \Delta y)) - (f(x_0 + \Delta x, y_0) - f(x_0, y_0)) = 2(y_0 + \Delta y) - 2y_0 = (\text{по теореме Лагранжа}) = L_y(y_0 + \theta_1)\Delta y = (f'_y(x_0 + \Delta x, \theta_1) - f'_y(x_0, \theta_1))\Delta y = (f''_{xy}(\theta_2, \theta_1)\Delta x)\Delta y = f''_{xy}(\theta_2, \theta_1)\Delta x\Delta y \implies \dots \implies f''_{xy}(\theta_2, \theta_1)\Delta x\Delta y = f''_{yx}(\theta_3, \theta_4)\Delta y\Delta x \iff f''_{xy}(\theta_2, \theta_1) = f''_{yx}(\theta_3, \theta_4) \iff \dots \iff f''_{yx}(x_0, y_0) = f''_{xy}(x_0, y_0)$

Общий случай:
$$
{\delta^k f \over \displaystyle\prod_{j = 1}^k \delta x_{i_j}}
$$

Если зафисксировать все переменные, кроме двух, то сводится к предыдущему

Пусть $f(x,y,z)$ имеет в окрестности $X(x,y,z)$ все непрерывные частные производные 1-го порядка  
$$
\Delta f = f(x + \Delta x, y + \Delta y, z + \Delta z) - f(x, y, z) = \\
f(x + \Delta x, y + \Delta y, z + \Delta z) - f(x, y + \Delta y, z + \Delta z) + f(x, y + \Delta y, z + \Delta z) + f(x, y, z + \Delta z) - f(x, y, z + \Delta z) - f(x, y, z) \\
= f'_x(\theta_1, y + \Delta y, z + \Delta z)\Delta x + f'_y(x, \theta_2, z + \Delta z)\Delta y + f'_z(x, y, \theta_3)\Delta z \\
= (f'_x(x, y, z) + \epsilon_x)\Delta x + (f'_y(x, y, z) + \epsilon_y)\Delta y + (f'_z(x, y, z) + \epsilon_z)\Delta z \\
= \lim\limits_{\Delta \rho \to 0} (\epsilon_x{\Delta x \over \Delta \rho} + \epsilon_x{\Delta x \over \Delta \rho}+ \epsilon_x{\Delta x \over \Delta \rho}) = 0 \\

\\
\Delta \rho - \text{длина вектора приращения} \\
\epsilon_x = f'_x(\theta_1, y + \Delta y, z + \Delta z) - f'_x(x, y, z) \to 0 \text{ при } \Delta \rho \to 0 \\
\text{аналогично для } \epsilon_y, \epsilon_z
$$


## Дифференцируемость

Функция $f(X)$ называется дифференцируемой в точке $X$, если в некоторой окрестности $u(X)$ приращение функции $\Delta f$ может быть записано в виде $\Delta f(X) = \sum A_i\Delta X_i$, где $A_i$ не зависят от $\Delta X$

## Касательная плоскость

Пусть поверхность $S : z = f(x, y)$, где ${\delta f \over \delta x}, {\delta f \over \delta y}$ - непрерывные функции в $X_0$. Рассмотрим плоскость $\Pi : Z = f(X_0) + {\delta f \over \delta x}(X_0)(x - x_0) + {\delta f \over \delta y}(X_0)(y - y_0)$

$$
M = (x, y, f(x, y)) \\
N = (x, y, f(X_0) + {\delta f \over \delta x}(X_0)(x - x_0) + {\delta f \over \delta y}(X_0)(y - y_0)) \\
|M - N| = \dots = o(|X-X_0|)
$$

В случае $\R^n$:
$$
\Pi : \displaystyle\sum_{i = 1}^n {\delta F \over x_i}(X)(x - x_i) = 0 
$$

## Дифференциал

$f(X)$ - дифференцируема в $X \implies$ дифференциалом $f(X)$ называется главная линейная часть приращения функции и обозначается $df(X)$
$$
\Delta f(X) = \displaystyle\sum_{i = 1}^n A_i\Delta x_i + o(\Delta p) \\
\implies df(X) = \displaystyle\sum_{i = 1}^n A_i\Delta x_i \\
{\delta f \over \delta x_i}(X) = \lim\limits_{\Delta x_i \to 0} {\Delta f(X) \over \Delta x_i} = \dots = A_i \\
\Delta f = df + o(\Delta \rho)
$$

## Теорема о производной сложной функции

Пусть $f(X)$ дифференцируема в  $X$, $\phi_i(t)$ дифференцируемы в $t_0$, причём $x_i = \phi_i(t_0)$, тогда 
$$
{df(\phi_i(t), \dots)  \over dt}(t_0) = \sum {\delta t \over \delta x_i} {dx_i \over dt}(t_0)
$$

### Доказательство
*TODO*

## Теорема о дифференцируемости композиции (?)

Пусть $f(X)$ дифференцируема в $X$, функции $\phi_i(T)$ дифференцируемы в $T$, причём $x_i = \phi_i(T), X \in \R^n, T \in \R^m$  
Тогда $(f \circ \phi)(T)$ дифференцируема в $T$ и ${\delta f \over \delta t_j} = \displaystyle\sum_{j = 1}^n {\delta f \over \delta x_i} {delta x_i \over \delta t_j}\ \forall 1 \leq j \leq m$

### Производная по направлению

$$
f(x_1, \dots, x_n) \\
\vec n = (\alpha_1, \dots, \alpha_n) \\
\text{рассмотрим } f(X + t\vec n), t \in \R > 0 \\

{\delta f \over \delta n} - \text{производная по направлению } \vec n \\
{\delta f \over \delta n} = \lim\limits_{t \to +0} {f(X+t\vec n) - f(X) \over t} = \\
= \displaystyle\sum_{i = 1}^n {\delta t \over \delta x_i}{dx_i \over dt} = \overrightarrow{grad} f * \vec n, \overrightarrow{grad} f = ({\delta f \over \delta x_i}, \dots) \\
{\delta f \over \delta \vec n} = \overrightarrow{grad} * \vec n = \sum {\delta f \over \delta x_i} \cos \alpha_i
$$

> повернхностью уровня функции $f(X)$ называется уравнение $f(X) = C$, где $C \in \R$ - константа

> Вектор $\overrightarrow{grad} f(X)$ направлен в сторону предельного изменения функции

> Вектор $\overrightarrow{grad} f(X)$ ортогонален поверхности уровня $f$, проходящей через $X$ $\implies \overrightarrow{grad} f(X)$ - вектор нормали касательной плоскости $f(X)$

### Свойства дифференциала
$$
df(X) = \displaystyle\sum_{i = 1}^n {\delta t \over \delta x_i}\Delta x_i = \displaystyle\sum_{i = 1}^n {\delta t \over \delta x_i}dx_i
$$


*те же, что и у производных?*
* $d(f + g) = df + dg$
* $d(f * g) = df * g + dg * f$
* $d{f \over g} = {gdf - fdg \over g^2}$
* "инвариантность 1-го дифференциала" (а записывать лень)

---
$$
d^2 f(X) = d(d\,f(X)) = d (\displaystyle\sum_{i=1}^n {\delta f\over \delta x}(X)dx_i)
$$

> Теорема. $d^k f(x) = (\displaystyle\sum_{i=1}^k {\delta \over \delta x_i} d_i)^kf(X)$  

## Формула Тейлора

$$
\Delta f(x) = df(x) + {d^2f(x)\over 2!} + \dots + {d^nf(x) \over n!} + \dots
$$

### Теорема

Пусть $X \in \R^n, f(X)$ определена в $u(X_0)$, имеет непрерывные частные производные в $u(X_0)$ вплоть до $k$-го порядка, тогда  
$$
\Delta f(X_0) = df(X_0) + {d^2f(X_0)\over 2!} + \dots + {d^kf(X_0) \over k!} + {d^{k+1}f(X_0 + \theta \Delta X) \over (k+1)!} \\
d^i(X_0) = (\displaystyle\sum {\delta \over \delta x_1}\Delta x_1)f(X_0)\ \forall i
$$

---

Доказать: $f^{(k)}(0) = 0$ для
$$
f(x) = \begin{cases}
e^{1 \over x} & x \neq 0
0 & x = 0
\end{cases} 
$$

---
## Точка локального экстремума
Точка $X_0$ -  локальный экстремиум для $f(X)$, если  
$$
\exists u_\epsilon(X_0) : (\forall x \in u_\epsilon(X_0)\ f(X) < f(X_0)) f(X) > f(X_0)
$$

## Матрица Гессе

Матрица $({\delta^2 f(x_0) \over \delta x_i \delta x_j}) = G_{ij}$ называется матрицей Гессе функции $f(X)$ в $X_0$

## Обобщённое скалярное произведение (симметричная билинейная форма)

Симметричной билинейной формой называется отображение $V^n \times V^n \to \R, (\vec a \to \vec b) \leadsto B(\vec a, \vec b) :$
* симметричность
* дистрибутивностью по сложению
* дистрибутивность по умножению на число (или это не так называется?)

$f(\vec a, \vec b) = \vec a B_ij \vec b^T$

### Примеры
* скалярное произведение - $B = E$ (единичная матрица)
* $B = -E$

### Квадратичная форма

$q(\vec X) = B(\vec X, \vec X)$ - квадратичная форма, ассоциированная с билинейной формой $B$.
* $q(\vec X)$ положительно определена $\iff q(\vec X) > 0\ \forall X \in V^n$
* $q(\vec X)$ отрицательно определена $\iff q(\vec X) < 0\ \forall X \in V^n$
* в противном случае $q(\vec X)$ - неопределённая

Всегда можно выбрать такой базис, что $B$ будет состоять из 1, -1 и 0 на главной диагонали  
$k, l, m$ - количество единиц, минус единиц и нулей в таком представлении - инварианты

### Критерий Сильвестра

*TODO*