# Rigid-ODE-systems-Population-dynamics
1а. Система ОДУ, описывающая изменение численности популяций двух видов и эволюцию некоего генетического признака $\alpha$ 
- Система ОДУ имеет вид:

$$\begin{equation*}
    \begin{cases}
        \dot{x} = x(1 - 0.5x - \frac{2}{7\alpha^2}y),~~~(a)\\
        \dot{y} = y(2\alpha - 3.5\alpha^2x - 0.5y),~~~(b)\\
        \dot{\alpha} = \varepsilon(2 - 7\alpha x),~~~(c)
    \end{cases}
    ~~~~~~~~~~~~~~~~(1)
\end{equation*}$$

- Параметры задачи таковы: 

$$\varepsilon \leqslant 0.01,~~~ 0 \leqslant x_0 \leqslant 3,~~~ 0 \leqslant y_0 \leqslant 15,~~~ \alpha_0 = 0,~~~ T_k = 1500.$$

Из (с) видно, что генетический признак изменяется медленней, чем численность популяций (решение - релаксационные колебания). 

1b. Более интересный случай - численность двух популяций зависит от взаимодействия между ними и двух медленно изменяющихся генетических признаков:

$$\begin{equation*}
    \begin{cases}
        \dot{x} = x(2\alpha_1 - 0.5x - \frac{\alpha_1^2}{\alpha_2^2}y)\\
        \dot{y} = y(2\alpha_2 - \frac{\alpha_2^2}{\alpha_1^2}x - 0.5y)\\
        \dot{\alpha_1} = \varepsilon(2 - \frac{2\alpha_1}{\alpha_2^2}y)\\
        \dot{\alpha_2} = \varepsilon(2 - \frac{2\alpha_2}{\alpha_1^2}x)
    \end{cases}
    ~~~~~~~~~~~(2)
\end{equation*}$$

- Параметры задачи таковы: 

$$\varepsilon \leqslant 0.01,~~~ 0 \leqslant x_0 \leqslant 40,~~~ 0 \leqslant y_0 \leqslant 40,~~~ \alpha_{10} = 0,~~~ \alpha_{20} = 10~~~ T_k = 2000.$$

Другой вариант (2):

$$\begin{equation*}
    \begin{cases}
        \dot{x} = x(2\alpha_1 - 0.5x - \frac{\alpha_1^3}{\alpha_2^3}y)\\
        \dot{y} = y(2\alpha_2 - \frac{\alpha_2^3}{\alpha_1^3}x - 0.5y)\\
        \dot{\alpha_1} = \varepsilon(2 - 3\frac{\alpha_1^2}{\alpha_2^3}y)\\
        \dot{\alpha_2} = \varepsilon(2 - 3\frac{\alpha_2^2}{\alpha_1^3}x)
    \end{cases}
\end{equation*}$$

- Параметры задачи таковы: 

$$\varepsilon \leqslant 0.001,~~~ 0 \leqslant x_0 \leqslant 40,~~~ 0 \leqslant y_0 \leqslant 40,~~~ \alpha_{10} = 0,~~~ \alpha_{20} = 10~~~ T_k = 2000.$$

a) Исследуем изменение двух видов (соответствующие численности - x, y и их генетических признаков $\alpha$, $\alpha_1$, $\alpha_2$) в зависимости от времени $t$, построим зависимости $x(t), y(t), \alpha(t), \alpha_2(t), x(y)$.

b) Исследуем разностные схемы на сходимость по сетке. 

c) Используем для численного решения (1), (2), (3) **явные методы Рунге-Кутты 1-го и 4-го порядков точности**. 
