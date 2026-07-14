---
time: 2026-07-14T23:21
jp: z変換
en: Z-Transform
aliases:
  - "z変換"
  - "Z変換"
  - "ゼット変換"
tags:
  - 分野/信号処理
  - 分野/制御工学/古典制御
  - 要素/手法・アルゴリズム
up:
  - "[[_Word/integral-transform|積分変換]]"
sibling:
  - "[[_Word/laplace-transform|ラプラス変換]]"
  - "[[_Word/fourier-transform|フーリエ変換]]"
pair:
  - "[[_Word/inverse-z-transform|逆z変換]]"
person:
  - "[[_Name/lotfi-zadeh|ロトフィ・ザデー]]"
  - "[[_Name/john-ragazzini|ジョン・ラガッツィーニ]]"
source:
  - "https://ja.wikipedia.org/wiki/Z変換"
---
# z変換（Z-Transform）
> 離散時間信号 $f(k)$ を複素変数 $z$ の関数 $F(z)$ に変換する数学的手法．ラプラス変換の離散時間版にあたる．

## 定義
片側z変換
$$
F(z) = \sum_{k=0}^\infty f(k)z^{-k}
$$
## 性質
- z変換は，離散時間系の差分方程式を代数方程式に変換する
- （ラプラス変換の離散時間版のような概念）
- ラプラス変換の変数 $s$ とz変換の変数 $z$ は，$z = e^{sT}$ で結ばれる．
- $s$ 平面の左半平面は，$z$ 平面の単位円内部に対応する．
- 離散時間系の安定条件は，「全ての極が $z$ 平面の単位円内部にある」こと
- z変換で得られた伝達関数に，$z = e^{j\omega T}$ を代入すると，離散時間フーリエ変換に一致する．

## 無限等比級数の公式
z変換の公式を適用すると，等比数列となるので，和の公式が使われる．  
$$
無限等比数列の和 = \frac{初項}{1-公比}
$$

## 例題
### 1. 等比型
$f(k) = 1$  
$$
\begin{align*}
F(z) &= \sum_{k=0}^\infty 1 \cdot z^{-k} \\
&= 0 + z^{-1} + z^{-2} + z^{-3} + \cdots \\
&= \frac{z^{-1}}{1-z^{-1}} \\
&= \frac{1}{z-1}
\end{align*}
$$

### 2. 等比型
$f(k) = \frac{1}{4^k} = 4^{-k}$  
$$
\begin{align*}
F(z) &= \sum_{k=0}^\infty 4^{-k} \cdot z^{-k} \\
&= 1 + 4^{-1}z^{-1} + 4^{-2}z^{-2} + 4^{-3}z^{-3} + \cdots \\
&= \frac{1}{1-4^{-1}z^{-1}} \\
&= \frac{z}{z-\frac{1}{4}} \\
&= \frac{4z}{4z-1}
\end{align*}
$$
### 3. 階差型
$f(k) = ke^{-k}$  
$$
\begin{align*}
F(z) &= \sum_{k=0}^\infty ke^{-k} \cdot z^{-k} \\
&= e^{-1}z^{-1} + 2e^{-2}z^{-2} + 3e^{-3}z^{-3} + \cdots \tag{1} \\
\end{align*}
$$

ここで，(1) は階差数列なので，等比 $e^{-1}z^{-1}$ を掛けた $\{e^{-1}z^{-1} \}F(z)$ を考える．

$$
\{e^{-1}z^{-1} \}F(z) = e^{-2}z^{-2} + 2e^{-3}z^{-3} + 3e^{-4}z^{-4} + \cdots \tag{2}
$$

(1) - (2) を求め，階差を等比数列へ落とし込む

$$
\begin{align*}
(1) - (2) 
&= F(z) - \{e^{-1}z^{-1} \}F(z) \\
&= e^{-1}z^{-1} + e^{-2}z^{-2} + e^{-3}z^{-3} + \cdots \\
\end{align*}
$$

右辺に等比級数の公式を適用して，

$$
\begin{align*}

F(z) \{ 1 -e^{-1}z^{-1} \} &= \frac{e^{-1}z^{-1}}{1-e^{-1}z^{-1}} \\
\Rightarrow F(z) &= \frac{e^{-1}z^{-1}}{(1-e^{-1}z^{-1})^2} \\
&= \frac{ez}{(ez - 1)^2}

\end{align*}
$$
