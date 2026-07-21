---
time: 2026-07-21T10:44
jp: ヤコビ行列
en: Jacobian Matrix
aliases:
  - "ヤコビ行列"
  - "ヤコビアン"
  - "関数行列"
  - "Jacobian"
tags:
  - 分野/数学/解析学
  - 分野/機構学
  - 要素/モデル・数式
up:
  - "[[_Word/partial-derivative|偏微分]]"
sibling:
  - "[[_Word/hessian-matrix|ヘッセ行列]]"
  - "[[_Word/gradient|勾配]]"
pair:
person:
  - "[[_Name/carl-gustav-jacob-jacobi|カール・グスタフ・ヤコブ・ヤコビ]]"
source:
  - "https://manabitimes.jp/math/1209"
---
# ヤコビ行列（Jacobian Matrix, $J$）
> 多変数ベクトル値関数の各成分を各変数で偏微分した値を並べた行列．1変数関数における微分係数（接線の傾き）の多変数版にあたる．

## ロボット機構学において[^1]
$n$ 個の変数で値が決まる $m$ 個の関数 $f_1 (x_1, x_2, \cdots , x_n), f_2 (x_1, x_2, \cdots , x_n), \cdots, f_m (x_1, x_2, \cdots , x_n)$ に対して次の $m × n$ 行列 $J$ がヤコビ行列となる．  

$$
\boldsymbol{J} =
\begin{bmatrix}
\frac{\partial f_1}{\partial x_1} \frac{\partial f_1}{\partial x_2} \cdots \frac{\partial f_1}{\partial x_n} \\
\frac{\partial f_2}{\partial x_1} \frac{\partial f_2}{\partial x_2} \cdots \frac{\partial f_2}{\partial x_n} \\
\vdots \vdots \vdots \\
\frac{\partial f_m}{\partial x_1} \frac{\partial f_m}{\partial x_2} \cdots \frac{\partial f_m}{\partial x_n}
\end{bmatrix}
$$

次のように定義
- $f_1, f_2, \cdots, f_m$ ：ロボット先端の位置や姿勢  
- $x_1, x_2, \cdots, x_n$ ：各関節の変位  

ロボットの動作自由度と関節数は，実用上等しいことが多いので，よく $m = n$ に限定される．




[^1]: 
