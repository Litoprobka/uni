---
id: 4d4fmzi2179lcv3y81g2zu7
title: Сравнимость по модулю
desc: ''
updated: 1669630782664
created: 1669630782664
---

$$
x \equiv y \mod n \iff n | (x - y)
$$

Для каждого класса эквивалентости выбирается элемент-представитель.

$\Z_n = \lbrace \overline 0, \overline 1, \dots, \overline{n-1} \rbrace$ множество представителей классов эквивалентности


## Остаток от деления

*я безусловно этого не знал*

$$
a \in \Z, b \in \N, b > 1 \\
s \in \Z, a = sb + Г, 0 \leq Г \leq b, \text{ где Г - остаткок от деления}
$$

---

На $\Z_n$ можно ввести умножение и сложение ($Z_n$ - кольцо?)
* $\overline a + \overline b = (a + b) \mod n$
    * $\forall a, a', b, b' \in \Z_n\ a \equiv a', b \equiv b' \implies a + b \equiv a' + b'$
    * нейтральный элемент - $\overline 0$
    * обратный элемент для $\overline a = \overline{(n - a)}$
* $\overline a * \overline b = (a * b) \mod n$
    * коммутатативность, ассоциативность, нейтральный элемент и т.п.
    * $\overline a \neq 0, \overline b \neq 0 \overline a * \overline b = 0 \implies \overline a$ и $\overline b$ - делители нуля
* $\exists k : \overline a^k = 0 \implies \overline a$ - идэмпотентный остаток

### Теорема

$\overline a$ обратим $\iff a$ и $n$ взаимно простые $\iff НОД(a, b) = 1$


