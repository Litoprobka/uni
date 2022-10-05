---
id: 600fgnayut4rm69k2wpemzd
title: Функция (отображение)
desc: ""
updated: 1664962421100
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
- $B \subset Y -$ все биективные функции
  $$
  \begin{cases}
  k \neq m \implies |B|=0 \\
  k = m \implies |B|=A_k^k = P_k = k!
  \end{cases}
  $$

### Каноническая биекция между $\ 2^X$ и $ \lbrace 0, 1 \rbrace^X$

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

#### Доказательство для счётных множеств

Построим $F : 2^A \to \lbrace 0, 1 \rbrace^A: \text{пусть } F(\tilde A) = \lbrace (а, \chi_{\tilde A}(a)) \in A \times \lbrace 0, 1 \rbrace \rbrace$

Докажем сюръективность $F$.  
От противного: $F$ не сюръективна $\implies \exists \hat f = \lbrace (a, \chi_{\hat A}(a)) \in A \times \lbrace 0, 1 \rbrace \rbrace : (\nexists \hat A : F(\hat A) = \hat f)$  
Из определения $supp(f) \implies \exists! \chi_{\tilde A} \forall \tilde A \in A;$  
$|2^A| = | |$  
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

1.  у $f$ есть правая обратная функция $\iff f$ сюръективна  
     Доказательство.
    _ Пусть $f$ не сюръективна $\implies \exists y_0 \in Y : \forall x \in X f(x) \neq y_0 \implies f(g(y_0) = y_0 -$ противоречие
    _ $f$ сюръективна $\implies \forall y \in Y f^{-1}(y) \neq \emptyset;$ выберем любой $x \in f^{-1}(y)$ и назовём его $g(y)$ - _нужна аксиома выбора, в ZF-аксиоматике её нет_
    > 2. y $f$ есть левая обратная функция $\iff f$ инъективна
        Доказательство.
        * Пусть $f$ не инъективна $\implies \exists x_1, x_2 \in X : x_1 \neq x_2, f(x_1) = f(x_2);$ Пусть $f(x_1)f(x_2)=y_0 \implies g(f(x_1)) = x_1 \implies g(y_0) = x_1, g(f(x_2)) = x_2 \implies g(y_0) = x_2; x_1 \neq x_2 \implies$ противоречие
        * $\forall y in Y$ если $y \in f(X)$, то $\exists! x : f(x) = y$ - назовём его $g(y)$; если $y \notin f(X),$ то обозначим за $g(y)$ любой элемент $X$.

> Следствие / главная теорема. $f$ биективна $\iff$ у $f$ есть "настоящая" обратная функция $f^{-1} : Y \to X$:

- $f \circ f^{-1} = Id_Y$
- $f^{-1} \circ f = Id_X$

> Fun fact: функция называется инволютивной, если $f$ = $f^{-1}$

### Примеры

- вектор $\vec a$ задаёт движение плоскости $T_{\vec a} : П \to П$  
   $T_{\vec b} \circ T_{\vec a} = T_{\vec a + \vec b}$

---

> Множество биекций $f : X \to X$ обозначается $S(X)$ и называется множеством перестановок

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
