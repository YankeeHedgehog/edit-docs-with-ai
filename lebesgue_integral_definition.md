# ルベーグ積分の定義

## 1. 単関数とその積分

### 単関数の定義
集合 $E$ 上の非負値関数 $\phi$ が**単関数**であるとは、有限個の非負実数 $a_1, a_2, \ldots, a_n$ と互いに素な可測集合 $E_1, E_2, \ldots, E_n$ が存在して、
$$\phi(x) = \sum_{i=1}^{n} a_i \chi_{E_i}(x)$$
と表されることである。ここで $\chi_{E_i}$ は集合 $E_i$ の特性関数である。

### 単関数の積分
可測集合 $E$ 上の非負単関数 $\phi(x) = \sum_{i=1}^{n} a_i \chi_{E_i}(x)$ に対して、そのルベーグ積分を
$$\int_E \phi \, d\mu = \sum_{i=1}^{n} a_i \mu(E_i \cap E)$$
で定義する。ここで $\mu$ は測度である。

## 2. 非負可測関数の積分

### 非負可測関数のルベーグ積分
可測集合 $E$ 上の非負可測関数 $f$ に対して、そのルベーグ積分を
$$\int_E f \, d\mu = \sup\left\{\int_E \phi \, d\mu : 0 \leq \phi \leq f, \phi \text{ は単関数}\right\}$$
で定義する。

### 可積分性
非負可測関数 $f$ が $E$ 上で**可積分**であるとは、$\int_E f \, d\mu < +\infty$ が成り立つことである。

## 3. 一般の可測関数の積分

### 正部と負部
可測関数 $f$ に対して、その**正部** $f^+$ と**負部** $f^-$ を
$$f^+(x) = \max\{f(x), 0\}, \quad f^-(x) = \max\{-f(x), 0\}$$
で定義する。このとき $f = f^+ - f^-$ かつ $|f| = f^+ + f^-$ が成り立つ。

### 一般の可測関数のルベーグ積分
可測集合 $E$ 上の可測関数 $f$ に対して、$f^+$ と $f^-$ がともに $E$ 上で可積分であるとき、$f$ は $E$ 上で**可積分**であるといい、そのルベーグ積分を
$$\int_E f \, d\mu = \int_E f^+ \, d\mu - \int_E f^- \, d\mu$$
で定義する。

## 4. 重要な性質

### 線形性
$f, g$ が可積分ならば、任意の実数 $a, b$ に対して
$$\int_E (af + bg) \, d\mu = a\int_E f \, d\mu + b\int_E g \, d\mu$$

### 単調性
$f \leq g$ a.e. かつ両関数が可積分ならば
$$\int_E f \, d\mu \leq \int_E g \, d\mu$$

### 可測集合の分割
$E = E_1 \cup E_2$ かつ $E_1 \cap E_2 = \emptyset$ ならば
$$\int_E f \, d\mu = \int_{E_1} f \, d\mu + \int_{E_2} f \, d\mu$$

## 5. 収束定理

### 単調収束定理（Monotone Convergence Theorem）
非負可測関数列 $\{f_n\}$ が単調増加し、$f_n \to f$ a.e. ならば
$$\lim_{n \to \infty} \int_E f_n \, d\mu = \int_E f \, d\mu$$

### 疲労収束定理（Fatou's Lemma）
非負可測関数列 $\{f_n\}$ に対して
$$\int_E \liminf_{n \to \infty} f_n \, d\mu \leq \liminf_{n \to \infty} \int_E f_n \, d\mu$$

### 優収束定理（Dominated Convergence Theorem）
可測関数列 $\{f_n\}$ が $f$ に a.e. 収束し、可積分関数 $g$ が存在して $|f_n| \leq g$ a.e. が全ての $n$ に対して成り立つならば
$$\lim_{n \to \infty} \int_E f_n \, d\mu = \int_E f \, d\mu$$