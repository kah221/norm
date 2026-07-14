---
time: 2026-07-14T10:58
jp: 可観測性行列
en: Observability Matrix
aliases:
  - "可観測性行列"
  - "可観測行列"
tags:
  - 分野/制御工学/現代制御
  - 分野/数学/線形代数
  - 要素/モデル・数式
up:
  - "[[_Word/observability|可観測性]]"
sibling:
  - "[[_Word/controllability-matrix|可制御性行列]]"
pair:
  - "[[_Word/controllability-matrix|可制御性行列]]"
person:
  - "[[_Name/rudolf-kalman|ルドルフ・カルマン]]"
source:
  - "https://blog.control-theory.com/entry/2024/01/29/154815"
---
# 可観測性行列（Observability Matrix, $\boldsymbol{U}_o$）
> システムの可観測性を判定するために，$\boldsymbol{A}$ 行列と $\boldsymbol{C}$ 行列から構成される行列 $\boldsymbol{U}_o$

## 定義式
$$
\boldsymbol{U}_o =
\begin{bmatrix}
	\boldsymbol{C} \\
	\boldsymbol{CA} \\
	\boldsymbol{CA}^2 \\
	...\\
	\boldsymbol{CA}^{n-1}
\end{bmatrix}
$$
- 型：$nr$ × $n$ 行列（← $r$ は出力数）

## 判定
階級（ランク）
- $\mathrm{rank}\: \boldsymbol{U}_o = n$ 　可観測
- $\mathrm{rank}\: \boldsymbol{U}_o < n$ 　不可観測

## 意味
- 各行 $\boldsymbol{CA}^k$ は，「出力 $y$ を $k$ 回微分した時に状態のどの成分が見えるか」を表す．
- $n$ ほんの行ベクトル $\boldsymbol{C}, \boldsymbol{CA}, \boldsymbol{CA}^2, ..., \boldsymbol{CA}^{n-1}$ が状態空間を"張る"（ランクが $n$ ）のとき，
	- 出力の観測から全状態変数を復元可能であることを意味する．  


[可制御性行列](_Word/controllability-matrix.md)とは双対の関係