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

冗長マニピュレータの[逆運動学](_Word/inverse-kinematics.md)では，[ヤコビ行列](_Word/jacobian-matrix.md)が正方行列にならないため通常の逆行列が定義できない．  
代わりに疑似逆行列 $\boldsymbol{J}^+$ を用いて $\boldsymbol{\dot{q}} = \boldsymbol{J}^+ \boldsymbol{\dot{r}}$ として関節速度の最小ノルム解を求める．  
（ $\boldsymbol{q}$：各関節，$\boldsymbol{r}$：手先 ）

- $\boldsymbol{A}$：$m × n$  行列
- $\boldsymbol{X}$：$n × m$  行列  
次の2つの行列を前提として，次の4式を満たす行列 $\boldsymbol{X}$ を一般化逆行列と呼ぶ．  
1. $\boldsymbol{AXA} = \boldsymbol{A}$  
2. $\boldsymbol{XAX} = \boldsymbol{A}$  
3. $(\boldsymbol{AX})^\top = \boldsymbol{AX}$  
4. $(\boldsymbol{XA})^\top = \boldsymbol{XA}$  

## 求め方
$\boldsymbol{A}$ がフルランクであれば，一般化逆行列 $\boldsymbol{A}^+$ が得られる．  

$$
\boldsymbol{A}^+ = 
\left\{
\begin{array}
\boldsymbol{A}^\top [\boldsymbol{AA}^\top]^{-1} & m < n \\
\boldsymbol{A}^{-1} & m = n \\
[\boldsymbol{A^\top A}]^{-1} \boldsymbol{A}^\top & m > n
\end{array}
\right\}
$$

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