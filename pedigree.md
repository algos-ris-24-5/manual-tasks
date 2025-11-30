$X_n$ — определитель матрицы $n$ порядка

$$
X_n = 
\begin{vmatrix}
-1 & 1 & 0 & \cdots & 0 & 0 \\
-6 & -1 & 1 & \cdots & 0 & 0 \\
0 & -6 & -1 & \cdots & 0 & 0 \\
\vdots & \vdots & \vdots & \ddots & \vdots & \vdots \\
0 & 0 & 0 & \cdots & -1 & 1 \\
0 & 0 & 0 & \cdots & -6 & -1
\end{vmatrix}
$$

Вывод рекуррентного соотношения:

Используем вычисление определителя разложением по строке:

$$
X_n = -1 \cdot X_{n-1} - 1 \cdot 
\begin{vmatrix}
-6 & 1 & 0 & \cdots & 0 & 0 \\
0 & -1 & 1 & \cdots & 0 & 0 \\
0 & -6 & -1 & \cdots & 0 & 0 \\
\vdots & \vdots & \vdots & \ddots & \vdots & \vdots \\
0 & 0 & 0 & \cdots & -1 & 1 \\
0 & 0 & 0 & \cdots & -6 & -1
\end{vmatrix}
$$

$$
= -1 \cdot X_{n-1} - 1 \cdot (-6 \cdot X_{n-2}) = -X_{n-1} + 6X_{n-2}
$$

(минор вычислен разложением по первому столбцу)

1 шаг (Составить и решить характеристическое уравнение):

$$
\lambda^n = -\lambda^{n-1} + 6\lambda^{n-2}
$$
$$
\lambda^2 = -\lambda + 6
$$
$$
\lambda^2 + \lambda - 6 = 0
$$
$$
\lambda_1 = 2 \quad \lambda_2 = -3
$$

2 шаг (Записать формулу решения рекуррентного соотношения в общем виде):

$$
X_n = C_1 \cdot 2^n + C_2 \cdot (-3)^n
$$

3 шаг (Найти неопределённые коэффициенты):

Найдём определители 1 и 2 порядка:

$$
X_1 = -1
$$

$$
X_2 = 
\begin{vmatrix}
-1 & 1 \\
-6 & -1
\end{vmatrix}
= 1 + 6 = 7
$$

Составим систему уравнений:

$$
\begin{cases}
-1 = 2C_1 - 3C_2 & \quad | \cdot 3 \\
7 = 4C_1 + 9C_2
\end{cases}
$$

Получаем:

$$
\begin{cases}
-3 = 6C_1 - 9C_2 \\
7 = 4C_1 + 9C_2
\end{cases}
$$

Сложим уравнения:

$$
10C_1 = 4 \quad \Rightarrow \quad C_1 = \dfrac{2}{5}
$$

Подставим $C_1$ во 2 уравнение:

$$
7 = \dfrac{8}{5} + 9C_2 \quad \Rightarrow \quad 9C_2 = \dfrac{27}{5} \quad \Rightarrow \quad C_2 = \dfrac{3}{5}
$$

Итоговая формула:

$$
X_n = \dfrac{2}{5} \cdot 2^n + \dfrac{3}{5} \cdot (-3)^n
$$

Рассчитаем определитель 10 порядка:

$$
X_{10} = \dfrac{2}{5} \cdot 2^{10} + \dfrac{3}{5} \cdot (-3)^{10} = 35839
$$

Ответ:  
$$
X_n = \dfrac{2}{5} \cdot 2^n + \dfrac{3}{5} \cdot (-3)^n
$$
$$
X_{10} = 35839
$$