---
time: 2026-07-24T14:13
jp: リンクヤコビ行列
en: Link Jacobian Matrix
aliases:
  - "リンクヤコビ行列"
  - "重心ヤコビ行列"
  - "重心ヤコビアン"
  - "Centroid Jacobian"
tags:
  - 分野/機構学
  - 分野/数学/解析学
  - 要素/モデル・数式
up:
  - "[[_Word/jacobian-matrix|ヤコビ行列]]"
sibling:
  - "[[_Word/denavit-hartenberg-parameters|DHパラメータ]]"
pair:
person:
source:
  - "https://www.kz.tsukuba.ac.jp/~isobe/181.pdf"
---
# リンクヤコビ行列（Link Jacobian Matrix）
> リンク機構の各リンクの重心と，能動関節（アクチュエータ）との速度関係を表すヤコビ行列．

$$
\boldsymbol{J}^k (q) = 
\begin{bmatrix}
\begin{array}{c|c}
\frac{\partial \boldsymbol{\bar{c}}_k}{\partial q_1} \cdots \frac{\partial \boldsymbol{\bar{c}}_k}{\partial q_k} & \boldsymbol{0} \\
\hline
\xi_1 \boldsymbol{z}_0 \cdots \xi_k \boldsymbol{z}_{k-1} & \boldsymbol{0}

\end{array}
\end{bmatrix}
$$

ここで，  
- $\boldsymbol{\bar{c}}_k$：第 $k$ リンクの重心を示すベクトル
- $\xi_i$：第 $i$ 関節が
	- 回転関節なら $1$
	- 並進関節なら $0$  

リンクヤコビ行列 $\boldsymbol{J}^k$ は第 $k$ 番目のリンクの重心の並進速度，角速度と関節速度の関係を表す．  
通常の[ヤコビ行列](_Word/jacobian-matrix.md)は，基底から先端の関係であるのに対し，リンクヤコビ行列は，各リンクごとの関係を表す．  

## 例 6自由度ロボットの場合
> 位置と姿勢合わせた6自由度

リンクヤコビ行列は

後で書く 260724_1438

$$
%%  %%\boldsymbol{J}^k = 
%%  %%\begin{bmatrix}
%%  %%\begin{array}{c|c}
%%  %%\frac{\partial \boldsymbol{\bar{c}}_k}{\partial q_1}
%%  %%
%%  %%\end{array}
%%  %%\end{bmatrix}
$$