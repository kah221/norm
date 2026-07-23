---
time: 2026-07-22T22:17
jp: DHパラメータ
en: Denavit-Hartenberg Parameters
aliases:
  - DHパラメータ
  - デナビット・ハーテンバーグパラメータ;DH記法;DH法
tags:
  - 分野/機構学
  - 要素/手法・アルゴリズム
up:
  - "[[_Word/forward-kinematics|順運動学]]"
sibling:
  - "[[_Word/homogeneous-transformation-matrix|同次変換行列]]"
  - "[[_Word/jacobian-matrix|ヤコビ行列]]"
pair:
person:
  - "[[_Name/jacques-denavit|ジャック・デナビット]]"
  - "[[_Name/richard-hartenberg|リチャード・ハーテンバーグ]]"
source:
  - https://www.jsme.or.jp/jsme-medwiki/doku.php?id=14:1008746
---
# DHパラメータ（Denavit-Hartenberg Parameters）
> ロボットマニピュレータなどのリンク機構における各リンク間の運動学的な関係を，4つのパラメータを導入することによって体系的に記述する方法．

直列リンク機構の隣接する関節軸 $i$ と $i + 1$ に対して，各リンクの幾何学的関係を4つのパラメータで記述する．  
隣接する2つの座標系 $\Sigma_{i-1}$ と $\Sigma_{i}$ の間の変換を，4段階に分割する．

- $\theta_i$：関節角度
- $d_i$：リンクオフセット
- $a_i$：リンク長さ
- $\alpha_i$：リンクねじれ角  

↓より具体的に...  

- $\theta_i$：（ $\boldsymbol{T}_{z\theta}$ ）$\Sigma_{i-1}$ を $z_{i-1}$ 軸まわりに $\theta_i$ 回転
- $d_i$：（ $\boldsymbol{T}_{zd}$ ）$\Sigma_{i-1}$ を $z_{i-1}$ 軸方向に $d_i$ 並進
- $a_i$：（ $\boldsymbol{T}_{xa}$ ）$\Sigma_{i-1}$ を $x_i$ 軸方向に $a_i$ 並進
- $\alpha_i$：（ $\boldsymbol{T}_{x\alpha}$ ）$\Sigma_{i-1}$ を $x_i$ 軸まわりに $\alpha_i$ 回転  

↓それぞれ座標変換行列に（参照：[回転行列](_Word/rotation-matrix.md)）

$$
\begin{align*}
\boldsymbol{T}_{z\theta} &=
	\begin{bmatrix}
	\begin{array}{ccc|c}
	C_{\theta i} & -S_{\theta i} 0 & 0 & 0 \\
	S_{\theta i} & C_{\theta i} 0 & 0 & 0 \\
	0 & 0 & 1 & 0 \\
	\hline
	0 & 0 & 0 & 1
	\end{array}
	\end{bmatrix}
\\\\
\boldsymbol{T}_{dz} &=
	\begin{bmatrix}
	\begin{array}{ccc|c}
	1 & 0 & 0 & 0 \\
	0 & 1 & 0 & 0 \\
	0 & 0 & 1 & d_i \\
	\hline
	0 & 0 & 0 & 1
	\end{array}
	\end{bmatrix}
\\\\
\boldsymbol{T}_{xa} &=
	\begin{bmatrix}
	\begin{array}{ccc|c}
	1 & 0 & 0 & a_i \\
	0 & 1 & 0 & 0 \\
	0 & 0 & 1 & 0 \\
	\hline
	0 & 0 & 0 & 1
	\end{array}
	\end{bmatrix}
\\\\
\boldsymbol{T}_{z\alpha} &=
	\begin{bmatrix}
	\begin{array}{ccc|c}
	1 & 0 & 0 & 0 \\
	0 & C_{\alpha i} & -S_{\alpha i} & 0 \\
	0 & S_{\alpha i} & C_{\alpha i} & 0 \\
	\hline
	0 & 0 & 0 & 1
	\end{array}
	\end{bmatrix}
\end{align*}
$$

## DHパラメータ→座標変換行列
4段階の操作は，行列として右からかけていくことで[同次変換行列](_Word/homogeneous-transformation-matrix.md) $^{i-1}\boldsymbol{T}_i$ が得られる．  
（3次元空間なら6自由度だが，DHパラメータなら4つでok）  

$$
\begin{align*}
^{i-1}\boldsymbol{T}_i &= \boldsymbol{T}_{z\theta} \; \boldsymbol{T}_{zd} \;\boldsymbol{T}_{xa} \; \boldsymbol{T}_{x\alpha} \\
&=
\begin{bmatrix}
\begin{array}{ccc|c}
C_{\theta i} & -S_{\theta i}C_{\alpha i} & S_{\theta i}S_{\alpha i} & a_i C_{\theta i} \\
S_{\theta i} & C_{\theta i}C_{\alpha i} & -C_{\theta i}S_{\alpha i} & a_i S_{\theta i} \\
0 & S_{\alpha i} & C_{\alpha i} & d_i \\
\hline
0 & 0 & 0 & 1
\end{array}
\end{bmatrix}
\end{align*}
$$

