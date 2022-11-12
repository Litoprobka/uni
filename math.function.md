---
id: 600fgnayut4rm69k2wpemzd
title: Функция (отображение)
desc: ''
updated: 1667817153705
created: 1663227151799
---

Функция $f$ из множества $A$ в множество $B$ ($f : A \to B$) - это:

> Правило, сопоставляющее каждому элементу $a \in A$ некотрый однозначно определённый элемент $b \in B$, который называется образом элемента $a$ при отображении $f$ и обозначается $f(a); \forall a \in A \, \exists! b \in B : f(a) = b$

## Примеры

1. школьные функции: $A=B=\R$, правило - формула, напр. $f(x) = x^2-2x+3$
2. $A=[0, +\infty], \, B=\R$, правило $f(x)=\sqrt x$
3. $A - \text{люди в аудитории},\, B=\N,\, f(x) = \text{рост } x$
4. $A - \text{множество студентов},\, B - \text{множество групп},\, f(x) = \text{в какой группе учится } x$
5. $A - \text{жители Москвы},\, B - \text{дома Москвы},\, f(x) - \text{дом, где живёт } x$
6. $А,\,B$ те же, $f(x) = \text{дом, который построил } x$ - не функция!

## График функции

График $f = \lbrace (a, f(a)) \in A \times B \rbrace$

## Свойства

### Инъективность (мономорфизм)

$f(x) = f(y) \iff x = y$  
равнозначно  
$x \neq x' \iff f(x) \neq f(x')$

### Сюръективность (эпиморфизм)

$\forall y \in Y \exists x \in X : y = f(x)$

### Биективность (взаимноднозначное соответствие)

Она же "взаимоднозначное отображение"  
$f$ инъективна $\land$ $f$ сюрьективна $\iff$ $f$ биективна  
$\forall x \exists! y : y=f(x) \\
\forall y \exists! x : f(x)=y$

#### Лемма про равномощные X и Y

_На семинарах / лекциях нам её не давали, но мне она кажется полезной_  
Если $f$ инъективна или сюръективна и $|X| = |Y|$, то $f$ биективна

- для инъективности  
  $(f(x) = f(x') \iff x = x') \implies$ для $|X|$ элементов $y \in Y$ $\exists! x : y = f(x); |X| = |Y| \implies \forall y \in Y \exists x : y = f(x) \implies f$ сюръективна $\implies f$ биективна
- для сюръективности  
  $(\forall y \in Y \exists x \in X : y = f(x)); \implies$ если $(\exists x \neq x' \in X : f(x) = f(x')$, то $|X| > |Y| \implies \text{противоречие}) \implies f$ инъективна $\implies f$ биективна

#### Образ отображения

$Im\,f = \lbrace y \in Y :\,\exists x \, f(x) = y \rbrace$

## Множество всех возможных функций $\ f : X \to Y$

$\lbrace f : X \to Y \rbrace$ oбозначается $Y^X$

Пусть $|X|=m, |Y|=k,$ тогда:

- $|Y^X|=k^m$
- $I \subset Y -$ все инъективные функции
  $$
  \begin{cases}
  k < m \implies |I|=0 \\
  k \geq m \implies |I|=A_k^m = k! / (k-m)!
  \end{cases}
  $$
- $S \subset Y -$ все сюръективные функции
  $$
  \begin{cases}
  m < k \implies |S|=0 \\
  m \geq k \implies ? \text{ "формула сложная, напишем потом"}
  \end{cases}
  $$
  *TODO: как запихнуть ссылку в формулу?*
- $B \subset Y -$ все биективные функции
  $$
  \begin{cases}
  k \neq m \implies |B|=0 \\
  k = m \implies |B|=A_k^k = P_k = k!
  \end{cases}
  $$

### Каноническая биекция между $\ 2^X$ и $\ \lbrace 0, 1 \rbrace^X$

$f: X \to \lbrace 0, 1 \rbrace$ - характеристическая (индикаторная) функция  
Пусть $A \subset X$, тогда индикаторная функция $\chi_A : X \to \lbrace 0, 1 \rbrace$; $$\chi_a = \begin{cases}
x \in A \to 1 \\
x \notin A \to 0
\end{cases}$$

$\chi_\emptyset(x)=0$  
$\chi_X(x)=1$

$f : X \to \lbrace 0, 1 \rbrace$ сопоставимо с множеством $\lbrace x \in X : f(x) = 1 \rbrace$, которое называется носителем $f$ ($ supp(f)$).

- $F : A \in 2^X \leadsto \chi_A$
- $G : f \leadsto supp(f) \in 2^X$
- $G \circ F = Id_{2^X}$
- $F \circ G = Id_{\lbrace 0, 1 \rbrace}$

$\chi_{[0, +\infty)}$ - функция Хевисайда

- если $X$ - конечное множество, $|Y|=2$, то между $Y^X$ и $2^X$ существует взаимооднозначное отображение
  - на самом деле, для бесконечных $X$ это тоже верно

## Характеристические функции + операции над множествами

$A, B \in 2^\Omega$  
Как выразить $\chi_{A \cap B}, \chi_{A \cup B}, \chi_{\overline A}$?
$$
\chi_{\overline A} = 1 - \chi_A \\
\chi_{A \cap B} = \chi_A * \chi_B \\
\chi_{A \cup B} = (\chi_A + \chi_B) \% 2 \\
\chi_{A \cup B} = \chi_{\overline {\overline A \cap \overline B}} = 1 - \chi_{\overline A \cap \overline B} = 1 - \chi_{\overline A} \chi_{\overline B} = \chi_A + \chi_B - \chi_{A \cap B}
$$

#### Доказательство для счётных множеств

Построим $F : 2^A \to \lbrace 0, 1 \rbrace^A: \text{пусть } F(\tilde A) = \lbrace (а, \chi_{\tilde A}(a)) \in A \times \lbrace 0, 1 \rbrace \rbrace$

Докажем сюръективность $F$.  
От противного: $F$ не сюръективна $\implies \exists \hat f = \lbrace (a, \chi_{\hat A}(a)) \in A \times \lbrace 0, 1 \rbrace \rbrace : (\nexists \hat A : F(\hat A) = \hat f)$  
Из определения $supp(f) \implies \exists! \chi_{\tilde A} \forall \tilde A \in A;$  
$|2^A| = |\lbrace 0, 1 \rbrace^A|$ - *что здесь должно быть написано?*  
 $\forall \hat A \exists \hat f = F(\hat A)$

Докажем инъективность $F$.  
От противного:  
$\exists \tilde A_1 \neq \tilde A_2 : F(\tilde A_1) = F(\tilde A_2) \\
\iff \lbrace (а, \chi_{\tilde A_1}(a)) \in A \times \lbrace 0, 1 \rbrace \rbrace = \lbrace (а, \chi_{\tilde A_2}(a)) \in A \times \lbrace 0, 1 \rbrace \rbrace \\
\iff \forall a \in A \,\exists!b_1, b_2 : \chi_{\tilde A_1}(a) = \chi_{\tilde A_2}(a) \\
\iff supp(\chi_{\tilde A_1}) = supp(\chi_{\tilde A_2}) \\
\iff \tilde A_1 = \tilde A_2 \\
\iff$ противоречие

Докажем сюръективность $F$.
От противного: пусть $\exists \hat f : (\nexists \hat A : F(\hat A) = \hat f$
$F$ инъективна, $|2^А| = |\lbrace 0, 1 \rbrace ^ A| \implies F$ сюръективна по [[лемме о равномощности | math.function#лемма-про-равномощные-x-и-y]].

## Композиция функций

Пусть $f : X \to Y, g : Y \to Z$  
$x \leadsto g(f(x)) -$ композиция $f$ и $g$  
$g \circ f : X \to Z$

### Свойства

- коммутативности в общем случае нет
- ассоциативность: $(h \circ g) \circ f = h \circ (g \circ f)$
  - $((h \circ g) \circ f)(x) = (h \circ g)(f(x)) = h(g(f(x)))$
  - $(h \circ (g \circ f))(x) = h((g \circ f)(x)) = h(g(f(x)))$

### Tождественная функция (identity)

$Id_Y \circ f = f, f \circ Id_X = f$  
$Id_X : X \to X, Id(x) = x$

Если $f : X \to X,$ то $Id_X \circ f = f \circ Id_X = f$

### Обратная функция

Можно ли найти такую $g : Y \to X$, что:

- $g \circ f = Id_X -$ левая обратная функция для $f$ $(\forall y \in Y f(g(y))=y)$
- $f \circ h = Id_Y -$ правая обратная функция для $f$

> Теорема. $f : X \to Y$

1. у $f$ есть правая обратная функция $\iff f$ сюръективна  
     Доказательство.
    _Пусть $f$ не сюръективна $\implies \exists y_0 \in Y : \forall x \in X f(x) \neq y_0 \implies f(g(y_0) = y_0 -$ противоречие
    _ $f$ сюръективна $\implies \forall y \in Y f^{-1}(y) \neq \emptyset;$ выберем любой $x \in f^{-1}(y)$ и назовём его $g(y)$ - _нужна аксиома выбора, в ZF-аксиоматике её нет_
    >
    > 2. y $f$ есть левая обратная функция $\iff f$ инъективна
        Доказательство.
        *Пусть $f$ не инъективна $\implies \exists x_1, x_2 \in X : x_1 \neq x_2, f(x_1) = f(x_2);$ Пусть $f(x_1)f(x_2)=y_0 \implies g(f(x_1)) = x_1 \implies g(y_0) = x_1, g(f(x_2)) = x_2 \implies g(y_0) = x_2; x_1 \neq x_2 \implies$ противоречие
        * $\forall y in Y$ если $y \in f(X)$, то $\exists! x : f(x) = y$ - назовём его $g(y)$; если $y \notin f(X),$ то обозначим за $g(y)$ любой элемент $X$.

> Следствие / главная теорема. $f$ биективна $\iff$ у $f$ есть "настоящая" обратная функция $f^{-1} : Y \to X$:

- $f \circ f^{-1} = Id_Y$
- $f^{-1} \circ f = Id_X$

> Fun fact: функция называется инволютивной, если $f$ = $f^{-1}$

### Примеры

- вектор $\vec a$ задаёт движение плоскости $T_{\vec a} : П \to П$  
   $T_{\vec b} \circ T_{\vec a} = T_{\vec a + \vec b}$

### Сюръективность и инъективность композиции функций
* $f, g$ - инъективны $\implies f \circ g$ инъективна
* $f, g$ - сюръективны $\implies f \circ g$ сюръективна

---

> Множество биекций $f : X \to X$ обозначается $S(X)$ и называется группой перестановок  
> Специальная запись для её элемента - $f = (^{1234}_{2143})$

## Образ и прообраз множества

Пусть $f : X \to Y, A \subset X, B \subset Y$

> $f(A) -$ образ множества $A, f(A)=\lbrace f(x) : x \in A \rbrace$  
> Прообраз множества $B$ - $f^{-1}(B) = \lbrace x : f(x) \in B \rbrace$

### Пример

$f : \R \to \R, f(x)=x^2$

- $f([0, 2])=[0,4]; f([-1, 2])=[0, 4]$
- $f^{-1}([0,9])=[-3,3]$

### Свойства

- $|A|=n \implies |f(A)|\leq n$
- $A \subset f^{-1}(f(A))$
- $\implies f(f^{-1}(B)) \subset B$
- $x \in f^{-1}(\lbrace f(x) \rbrace)$  
   Доказательство: возьмём $y \in f(f^{-1}(B)) \implies \exists x \in f^{-1}(B) : y = f(x); f(x) \in B \implies y \in B$

---

Пусть $Y_n = \lbrace 1, 2, 3...n \rbrace, X -$ любое  
$X^{Y_n}=\lbrace f : \lbrace 1..n \rbrace \to X \rbrace$  
$X \times X \times X \times ... \times X = \lbrace (x_1, x_2, x_3, ... x_n) : x_i \in X \rbrace$

- Для этих двух множеств существует биекция
- $Z^{X \cup Y} \to? Z^X \times Z^Y$
- $(Z^Y)^X \to? Z^{Y \times X}$

---

### Множество сюръекций $\ X \to Y$

_должно ли это быть в [[math.combinatorics]]?_

$$
|X|=n, |Y|=m, m \leq n \\
S \subset Y^X - \text{множество всех сюръективных функций} \\
|S| = ? \\
A_i = \lbrace f : X \to Y : f(X) \not\ni y \rbrace \\
S = Y^X \setminus \displaystyle\bigcap_{i=1}^m A_i \\
|A_i| = (m - 1)^n \quad f \in A_i, f : X \to Y \setminus \lbrace y_i \rbrace \\
|A_i \cap A_j| = (m - 2)^n \\
|\sum \chi_{A_i} - \sum \chi_{A_i \cap A_j} + \dots + (-1)^{k-1}\sum X_{\bigcap A_{i_k}}| = (m - k)^n \\
\implies |\bigcup A_m| = C_m^1(m - 1)^n - C_m^2(m - 2)^n + C_m^3(m - 3)^n + \dots + (-1)^{k+1}C_m^k(m - k)^n + \dots + (-1)^m m \\
\implies |S| = m^n - C_m^1(m - 1)^n + C_m^2(m - 2)^n + C_m^3(m - 3)^n + \dots + (-1)^{k}C_m^k(m - k)^n + \dots + (-1)^{m-1} m
$$

---
Пусть $S(X) -$ множество биекций $X \to X$  
Для $X = \lbrace 1, 2, 3, \dots, n \rbrace \quad S(X) = S_n(X) -$ симметрическая группа (группа перестановок)  
$|S_n| = n!$

## Задача о числе беспорядка
*вынести в отдельную запись*

Сколько есть $\phi \in S_n : \forall i\ \phi(i) \neq i$  
Пусть $W = \lbrace \phi \in S_n : \forall i\ \phi(i) \neq i \rbrace\, |W|=\ ?$  
Равносильный вопрос: $|S_n \setminus W| =\ ?$  
$$
A_i = \lbrace \phi \in S_n : \phi(i) = i \rbrace \\
S_n \setminus W = \displaystyle\bigcup_{i=1}^n A_i  
|A_i| = (n-1)! \\
|A_i \cap A_j| = (n-2)! \\
|\displaystyle\bigcap_{i=1}^k A_i| = (n-k)! \\
|\displaystyle\bigcup_{i=1}^n A_i| = \sum |A_i| - \sum |A_i \cap A_j| + \dots + (-1)^{k+1}\sum |(\displaystyle\bigcup_{i=1}^k A_i)| = \\
= \displaystyle\sum_{k=1}^n (-1)^{k+1}C_n^k (n - k)! \\
= n!\displaystyle\sum_{k=1}^n {(-1)^{k+1} \over k!} \\
\implies |W| = n!\displaystyle\sum_{k=1}^n {(-1)^k \over k!}
$$

Тогда вероятность того, что $\phi \in S_n$ также $\in W$ равна $\displaystyle\sum_{k=1}^n {(-1)^k \over k!} \approx e^{-1} \approx {1 \over e}$

---

## Экстремиум
_TODO_  
> $x_0$ - локальный максимум (минимум) функции $f(x) \iff \forall x \in u(x_0) f(x) < f(x_0)$

## Выпуклые вверх / вниз функции

> Функция $f(x)$ называется выпуклой вверх (вниз) в $x_0 \iff \exists u(x_0) : \forall x_1 \in u(x_0)\ f(x) < f(x_1) + f'(x_1)(x-x_1) (f(x) < f(x_1) + f'(x_1)(x-x_1) \text{для выпуклой вниз})$

> $f(x_1) + f'(x_1)(x-x_1)$ - уравнение касательной

$$
f(x) - (f(x_0) + f'(x_0)(x-x_0)) = {f''(\Theta) \over 2}(x-x_0)^2
$$

Т.е. если $f''(x_0) > 0, f''(x)$ - непрерывная, то $f(x)$ - выпуклая вверх

> Точки $x$, в которых $f''(x) = 0$ называются точками перегиба

### Ложная точка перегиба

_нужны картинки_

* $y = x^2$ - есть точка минимума, нет точки перегиба
* $y = x^3$ - есть ложный экстремум и точка перегиба
* $y = x^4$ - есть точка минимума и ложная точка перегиба


---

Пусть $f'(x_0)=f''(x_0)= \dots = f^{(k)}(x_0) = 0$  
$f(x) = \displaystyle\sum_{m = o}^k{f^{(m)}(x_0)^m \over m!} + {f{(k+1)(\Theta)} \over k + 1}(x - x_0)^{k+1} = f(x_0) + {f^{(k+1)}(\Theta) \over (k+1)!}(x-x_0)^{k+1}$  
_какие-то объёмные формулы_  
$$\begin{cases}
x_0 - \text{ максимум, если} & f^{(k+1)}(x_0) < 0  \\
x_0 - \text{ минимум, если} & f^{(k+1)}(x_0) > 0 \\
f^{(k+1)}(x_0) > 0 & f(x) \text{ возрастает в} x_0 \\
f^{(k+1)}(x_0) < 0 & f(x) \text{ убывает в} x_0
\end{cases}$$

## Асимптоты

Прямая $x=x_0$ называется вертикальной асимптотой для $f(x) \iff (\lim\limits_{x \to x_0 + 0} f(x) = \infty) \lor (\lim\limits_{x \to x_0 - 0} f(x) = \infty)$

_картинки_

### Примеры

* $y = {1 \over x}$, $x=0$ - верт. асимптота
* $y = {1 \over (x-1)^2(x-2)(x-3)^3}$

### Наклонные асимптоты

Прямая $y = kx + b$ называется асимтотой для $f(x)$ при $x \to +\infty$ ($x \to -\infty$) $\iff \exists \lim\limits_{x \to +\infty (-\infty)} (f(x)-(kx+b)) = 0$

### Существование асимптоты

$y = kx + b$ является наклонной асимптотой для $f(x)$ при $x \to +\infty (-\infty)$, если существуют два конечных предела: $\lim\limits_{x \to +\infty} {f(x) \over x} = k, \lim\limits_{x \to +\infty} (f(x) - kx) = b$

#### Доказательство

$\lim\limits_{x \to +\infty}{f(x) - (kx + b) \over x} = \lim\limits_{x \to +\infty}{f(x) \over x} - k - b/x = \lim\limits_{x \to +\infty}({f(x) \over x} - k) = 0$  
аналогично для $b$ (мне лень писать)