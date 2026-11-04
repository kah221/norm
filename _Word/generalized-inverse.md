---
time: 2026-07-24T14:40
jp: 一般化逆行列
en: Generalized Inverse
aliases:
  - "一般化逆行列"
  - "疑似逆行列"
  - "擬似逆行列"
  - "一般逆行列"
  - "Pseudoinverse"
tags:
  - 分野/数学/線形代数
  - 分野/機構学
  - 分野/制御工学/現代制御
  - 要素/モデル・数式
up:
  - "[[_Word/jacobian-matrix|ヤコビ行列]]"
sibling:
  - "[[_Word/inverse-matrix|逆行列]]"
pair:
person:
  - "[[_Name/e-h-moore|E・H・ムーア]]"
  - "[[_Name/roger-penrose|ロジャー・ペンローズ]]"
  - "[[_Name/arne-bjerhammar|アルネ・ビエルハンマル]]"
source:
  - "https://ja.wikipedia.org/wiki/ムーア・ペンローズ逆行列"
---
# 一般化逆行列（Generalized Inverse）
> 正方でない行列，あるいは正則でない（逆行列を持たない）行列に対しても定義できるよう，通常の逆行列の概念を一般化した行列．

冗長マニピュレータの逆運動学では，ヤコビ行列が正方行列にならないため通常の逆行列が定義できない．
代わりに疑似逆行列 $\boldsymbol{J}^+$ を用いて $\boldsymbol{\dot{q}} = \boldsymbol{J}^+ \boldsymbol{\dot{r}}$ として関節速度の最小ノルム解を求める．
（ $\boldsymbol{q}$：関節変位ベクトル，$\boldsymbol{r}$：手先の位置・姿勢ベクトル ）

## 定義（ムーア・ペンローズ一般化逆行列）
- $\boldsymbol{A}$：$m \times n$ 行列
- $\boldsymbol{X}$：$n \times m$ 行列

次の4式をすべて満たす行列 $\boldsymbol{X}$ を，ムーア・ペンローズ一般化逆行列（疑似逆行列）と呼び，$\boldsymbol{A}^+$ と書く．

1. $\boldsymbol{AXA} = \boldsymbol{A}$
2. $\boldsymbol{XAX} = \boldsymbol{X}$
3. $(\boldsymbol{AX})^\top = \boldsymbol{AX}$
4. $(\boldsymbol{XA})^\top = \boldsymbol{XA}$

$\boldsymbol{A}^+$ は任意の行列に対して存在し，一意に定まる．
（条件1だけを満たす行列も広義の「一般化逆行列」と呼ばれるが，こちらは一意に定まらない．）

## 求め方
$\boldsymbol{A}$ がフルランクのとき，$\boldsymbol{A}^+$ は次の式で計算できる．

$$
\boldsymbol{A}^+ =
\begin{cases}
\boldsymbol{A}^\top \left( \boldsymbol{A}\boldsymbol{A}^\top \right)^{-1} & (m < n,\ \text{行フルランク}) \\
\boldsymbol{A}^{-1} & (m = n,\ \text{正則}) \\
\left( \boldsymbol{A}^\top \boldsymbol{A} \right)^{-1} \boldsymbol{A}^\top & (m > n,\ \text{列フルランク})
\end{cases}
$$

- $m < n$：解が無数にある劣決定系．$\boldsymbol{x} = \boldsymbol{A}^+\boldsymbol{b}$ は，解の中でノルム $\|\boldsymbol{x}\|$ が最小のもの（最小ノルム解）
- $m > n$：解が存在しない過剰決定系．$\boldsymbol{x} = \boldsymbol{A}^+\boldsymbol{b}$ は，$\|\boldsymbol{Ax} - \boldsymbol{b}\|$ を最小にするもの（最小二乗解）
## 性質
$$
\begin{align*}
(\boldsymbol{A}^+)^+ &= \boldsymbol{A} \tag1 \\
(\boldsymbol{A}^\top)^+ &= (\boldsymbol{A^+})^\top \tag2 \\
(\boldsymbol{A} \boldsymbol{A}^\top)^+ &= (\boldsymbol{A}^+)^\top \boldsymbol{A}^+ \tag3 \\
\boldsymbol{A}^+ &= (\boldsymbol{A}^\top \boldsymbol{A})^+ \boldsymbol{A}^\top = \boldsymbol{A}^\top (\boldsymbol{A} \boldsymbol{A}^\top)^+ \tag4
\end{align*}
$$

$\boldsymbol{b} \in \boldsymbol{R}^m$  とすると

$$
\boldsymbol{A}\boldsymbol{x} = \boldsymbol{b}
$$

後で書く