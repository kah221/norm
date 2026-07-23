---
time: 2026-07-23T13:29
jp: 同次変換行列
en: Homogeneous Transformation Matrix
aliases:
  - "同次変換行列"
  - "座標変換行列;斉次変換行列"
  - "座標変換行列"
  - "斉次変換行列"
tags:
  - 分野/数学/線形代数
  - 分野/機構学
  - 要素/モデル・数式
up:
  - "[[_Word/rotation-matrix|回転行列]]"
sibling:
  - "[[_Word/denavit-hartenberg-parameters|DHパラメータ]]"
pair:
person:
  - "[[_Name/jacques-denavit|ジャック・デナビット]]"
  - "[[_Name/richard-hartenberg|リチャード・ハーテンバーグ]]"
source:
  - "https://kim-xps12.github.io/b-sky-lab/study/2021/08/07/DH-method.html"
---
# 同次変換行列（Homogeneous Transformation Matrix）
> 回転行列と並進ベクトルを1つの正方行列にまとめ，回転と並進を単一の行列積で同時に表現できるようにした行列．

## 定義（順方向）
3次元空間では4x4行列となる． 
「座標系 $n$ から座標系 $n-1$ の同次変換行列」

$$
^{n-1}\boldsymbol{T}_n = 
\begin{bmatrix}
\begin{array}{ccc|c}
	\\
	& ^{n-1}\boldsymbol{R}_n && ^{n-1}\boldsymbol{p}_n \\
	\\
	\hline
	0 & 0 & 0 & 1
\end{array}
\end{bmatrix}
$$

ここで，$\boldsymbol{p}$ は並進ベクトル，4行目の $[0 \: 0 \: 0 \: 1]$  は固定行．  
並進と回転両方を別々に扱うと合成計算が複雑になるが，同次座標（元の座標ベクトルに1を追加して4次元化した座標）を導入することで，回転と並進を1回の行列積で済ませられる．  

複数の座標変換を合成する際は，対応する同次変換行列 $^{n-1}\boldsymbol{T}_n$ を基部から先端へ順に掛け合わせていく．  

## 定義（逆方向）
> 順方向の定義の逆行列

「座標系 $n-1$ から座標系 $n$ の同次変換行列」

$$
(^{n-1}\boldsymbol{T}_n)^{-1} = 
\begin{bmatrix}
\begin{array}{ccc|c}
	\\
	& (^{n-1}\boldsymbol{R}_n)^\top && -(^{n-1}\boldsymbol{R}_n)^\top (^{n-1}\boldsymbol{p}_n) \\
	\\
	\hline
	0 & 0 & 0 & 1
\end{array}
\end{bmatrix}
$$

回転行列の逆行列=転置，また，並進部分には少し特別な変換 $-R^\top p$ が入る

## 表記
> $^{■}T_{▲}$ ：
> 　座標系▲を座標系■から見た変換行列  
> 　▲の姿勢を，■で表現した行列  
> 　→→ **「座標系▲から座標系■への座標変換」**
- 左上付き文字：誰から見て　を意味する
- 右下付き文字：誰を見て　を意味する
★隣接する文字の右下と左上の添え字が同じときに計算できる（この表記の利点）

## 全体座標系→手先座標系
基部からエンドエフェクタまでつなげる際は，右にかけていく
座標系0, 1, 2, ... n  のとき，手先座標系 $\Sigma_n$ で定義された座標を全体座標系 $\Sigma_{0}$ 表記にしたい．  
この時につかう同次変換行列の求め方  

$$
^0\boldsymbol{T}_n = ^0\boldsymbol{T}_1 ・ ^1\boldsymbol{T}_2 ・ ^2\boldsymbol{T}_3 \cdots ^{n-1}\boldsymbol{T}_n
$$


## 用途
### ①【B→A】座標系Bで表現された点pを座標系Aで表現しなおす
- $^B\boldsymbol{p}$：座標系Bで表現された，点pの座標（並進ベクトル 3x1）
- $^A\boldsymbol{T}_B$：座標系Bから座標系Aへの同次変換行列（4x4）
- $^A\boldsymbol{p}$：座標系Aで表現された，点pの座標（3x1）←求
- 2つの座標系A, Bは，並進と回転の両方を含んでいてもok
同次変換行列は4次元なので，並進ベクトルに第4行1を付加しておく．  

$$
\begin{bmatrix}
^{A}\boldsymbol{p} \\
\hline
1
\end{bmatrix}
= \:
^A\boldsymbol{T}_B ・
\begin{bmatrix}
^{B}\boldsymbol{p} \\
\hline
1
\end{bmatrix}
$$

### ②【A→B】座標系Aで表現された点pを座標系Bで表現しなおす
↑①の逆  
注：**逆行列**を使う（右からかけるのではない）  

$$
\begin{bmatrix}
^{B}\boldsymbol{p} \\
\hline
1
\end{bmatrix}
= \:
^A\boldsymbol{T}_B ^{-1} ・
\begin{bmatrix}
^{A}\boldsymbol{p} \\
\hline
1
\end{bmatrix}
$$

