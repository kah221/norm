---
time: 2026-07-23T13:19
jp: 回転行列
en: Rotation Matrix
aliases:
  - "回転行列"
  - "方向余弦行列"
  - "Direction Cosine Matrix"
tags:
  - 分野/数学/線形代数
  - 分野/機構学
  - 要素/モデル・数式
up:
  - "[[_Word/orthogonal-matrix|直交行列]]"
sibling:
  - "[[_Word/homogeneous-transformation-matrix|同次変換行列]]"
pair:
person:
  - "[[_Name/leonhard-euler|レオンハルト・オイラー]]"
source:
  - "https://ja.wikipedia.org/wiki/回転行列"
---
# 回転行列（Rotation Matrix）
> ユークリッド空間内における原点中心の回転変換を表す正方行列．

原点を通る軸回りの回転操作による座標変換を行列で表現したもの．  
回転変換は直交変換の一種．  
## 性質
- $\boldsymbol{R}^{-1} = \boldsymbol{R^\top}$
- $\mathrm{det}(\boldsymbol{R}) = 1$ 
- 直交行列：各行・列が互いに直行する単位ベクトルになっている
- （ $\mathrm{det}(\boldsymbol{R}) = -1$ となる直交行列は鏡映で，回転行列とは別）

## 回転方向の符号
> **右手座標系**とする  
> 「回転軸の正の方向から原点を見たとき，反時計回りが正」  
> ↑右手の親指を軸の正方向に向け，残りの4本の指が巻き付く方向!!!

## 2次元の場合
2次元の場合は，紙面に垂直な $z$ 軸まわりの回転としてのみ定義可能．
点 $(x, y)$ を原点中心に反時計回りを正として $\theta$ だけ回転した点の座標は，  
次の $\boldsymbol{R}_\theta$ を **左から** かけることで得られる．  

$$
\boldsymbol{R}_\theta = 
\begin{bmatrix}
\cos \theta & -\sin \theta \\
\sin \theta & \cos \theta
\end{bmatrix}
$$

## 3次元の場合
3次元の場合は，回転軸は $x, y, z$ の3つとりえるのでそれぞれ定義可能．  
★ $x, y, z$ 軸まわり回転は...→それぞれ行列の $(1, 1), (2, 2), (3, 3)$ 要素が $1$ になる．  

$x$ 軸まわりに $+\theta$ だけ回転
$$
\boldsymbol{R}_{x\theta} = 
\begin{bmatrix}
1 & 0 & 0 \\
0 & \cos \theta & -\sin \theta \\
0 & \sin \theta & \cos \theta
\end{bmatrix}
$$

$y$ 軸まわりに $+\theta$ だけ回転
$$
\boldsymbol{R}_{y\theta} = 
\begin{bmatrix}
\cos \theta & 0 & \sin \theta \\
0 & 1 & 0 \\
-\sin \theta & 0 & \cos \theta
\end{bmatrix}
$$

$z$ 軸まわりに $+\theta$ だけ回転
$$
\boldsymbol{R}_{z\theta} = 
\begin{bmatrix}
\cos \theta & -\sin \theta & 0 \\
\sin \theta & \cos \theta & 0 \\
0 & 0 & 1
\end{bmatrix}
$$
