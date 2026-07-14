---
time: 2026-07-14T10:57
jp: 可制御性行列
en: Controllability Matrix
aliases:
  - "可制御性行列"
  - "可制御行列"
tags:
  - 分野/制御工学/現代制御
  - 分野/数学/線形代数
  - 要素/モデル・数式
up:
  - "[[_Word/controllability|可制御性]]"
sibling:
  - "[[_Word/observability-matrix|可観測性行列]]"
pair:
  - "[[_Word/observability-matrix|可観測性行列]]"
person:
  - "[[_Name/rudolf-kalman|ルドルフ・カルマン]]"
source:
  - "https://blog.control-theory.com/entry/2024/01/29/154815"
---
# 可制御性行列（Controllability Matrix, $\boldsymbol{U}_c$）
> システムの可制御性を判定するために，$\boldsymbol{A}$ 行列と $\boldsymbol{B}$ 行列から構成される行列 $\boldsymbol{U}_c$ 

## 定義式
$$
\boldsymbol{U}_c =
\begin{bmatrix}
	\boldsymbol{B}, \boldsymbol{AB}, \boldsymbol{A^2B}, ..., \boldsymbol{A}^{n-1}\boldsymbol{B}
\end{bmatrix}
$$
- 型：$n$ × $nm$ 行列（← $m$ は入力数）

## 判定
階級（ランク）
- $\mathrm{rank}\: \boldsymbol{U}_c = n$ 　可制御
- $\mathrm{rank}\: \boldsymbol{U}_c < n$ 　不可制御

## 意味
- 各列 $\boldsymbol{A}^k \boldsymbol{B}$ は，「入力が $k$ ステップの時間遅延を経て状態空間のどの方向に影響御与えるか」を表す．
- $n$ 本のベクトル $\boldsymbol{B}, \boldsymbol{AB}, ..., \boldsymbol{A}^{n-1} \boldsymbol{B}$ が，状態空間全体を"張る"（ランクが $n$ ）とき，
	- 入力によって状態空間のあらゆる方向に到達可能であることを意味する．  


[可観測性行列](_Word/observability-matrix.md)とは双対の関係