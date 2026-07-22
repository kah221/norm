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
\frac{\partial f_1}{\partial x_1} & \frac{\partial f_1}{\partial x_2} & \cdots & \frac{\partial f_1}{\partial x_n} \\
\frac{\partial f_2}{\partial x_1} & \frac{\partial f_2}{\partial x_2} & \cdots & \frac{\partial f_2}{\partial x_n} \\
\vdots & \vdots & & \vdots \\
\frac{\partial f_m}{\partial x_1} & \frac{\partial f_m}{\partial x_2} & \cdots & \frac{\partial f_m}{\partial x_n}
\end{bmatrix}
$$

次のように定義
- $f_1, f_2, \cdots, f_m$ ：ロボット先端の位置や姿勢  
- $x_1, x_2, \cdots, x_n$ ：各関節の変位  
ロボットの動作自由度と関節数は，実用上等しいことが多いので，よく $m = n$ に限定される．
### 意味
- 各 $x_1 \sim x_2$ が，各 $f_1 \sim f_n$ に対してどれくらいの感度を持っているのか???

---
## 例）3自由度平面ロボットの[順運動学](_Word/forward-kinematics.md)

### 構造の説明
- 3つのリンクと3つの1自由度回転関節から構成される
- 3つのリンクは直列でつながっている
- 座標系（右手座標系．紙面に対し右が $x$）
	- $\Sigma_0$：全体座標系（全体座標軸に固定された座標系）
	- $\Sigma_1$：第1リンクに固定された座標系
	- $\Sigma_2$：第2リンクに固定された座標系
	- $\Sigma_3$：第3リンクに固定された座標系
- 量
	- $\theta_{1, 2, 3}$：各関節角（第 $n-1$ 座標系から見た第 $n$ 座標系の回転角度）←リンク角度，$\Sigma_0$ からの絶対角度ではない
	- $\phi_\mathrm{E}$：$\Sigma_0$ からみた第3リンクの回転角度（エンドエフェクタの角度）
	- $l_{1, 2, 3}$：第1, 2, 3リンクの長さ  

（中略．同時変換行列を用いて...）
### アーム先端 $\mathrm{E}$ の位置 $(x_E, y_E, z_E)$ と 先端向き $\phi_\mathrm{E}$ 
略式記号： $S_1 = \sin \theta_1 , \:\: C_{12} = \cos (\theta_1 + \theta_2)$  
$$
\begin{align*}
x_\mathrm{E} &= l_1C_1 + l_2C_{12} + l_3C_{123} \tag1 \\
y_\mathrm{E} &= l_1S_1 + l_2S_{12} + l_3S_{123} \tag2 \\
z_\mathrm{E} &= 0 \\
\\
\phi_\mathrm{E} &= \mathrm{atan2} \: (S_{123}, C_{123}) \\
&= \theta_1 + \theta_2 + \theta_3 \tag3
\end{align*}
$$

式(1) ~ (3)を時間 $t$ で微分し速度次元にすると

$$
\begin{align*}
\dot{x}_\mathrm{E} &= (-l_1S_1 - l_2S_{12} - l_3S_{123})\dot{\theta_1} + (-l_2S_{12} -l_3S_{123})\dot{\theta_2} + (-l_3S_{123})\dot{\theta_3} \\
\dot{y}_\mathrm{E} &= (l_1C_1 + l_2C_{12} + l_3C_{123})\dot{\theta_1} + (l_2C_{12} +l_3C_{123})\dot{\theta_2} + (l_3C_{123})\dot{\theta_3} \\
\dot{\phi}_\mathrm{E} &= \dot{\theta_1} + \dot{\theta_2} + \dot{\theta_3} \\
\end{align*}
$$

これを行列形式にすると次のようになり，係数部分がヤコビ行列となる．

$$
\begin{align*}
\begin{bmatrix}
\dot{x}_\mathrm{E} \\
\dot{y}_\mathrm{E} \\
\dot{\phi}_\mathrm{E}
\end{bmatrix}
&=
\begin{bmatrix}
-l_1S_1 - l_2S_{12} - l_3S_{123} & -l_2S_{12} -l_3S_{123} & -l_3S_{123} \\
l_1C_1 + l_2C_{12} + l_3C_{123} & l_2C_{12} +l_3C_{123} & l_3C_{123}\\
1 & 1 & 1
\end{bmatrix}
\begin{bmatrix}
\dot{\theta_1} \\
\dot{\theta_2} \\
\dot{\theta_3}
\end{bmatrix}
\\
\begin{bmatrix}
\dot{x}_\mathrm{E} \\
\dot{y}_\mathrm{E} \\
\dot{\phi}_\mathrm{E}
\end{bmatrix}
&= \boldsymbol{J}
\begin{bmatrix}
\dot{\theta_1} \\
\dot{\theta_2} \\
\dot{\theta_3}
\end{bmatrix}
\end{align*}
$$

速度は，ある微小時間における各関節と，先端の位置・姿勢の微小変化量とも捉えられる．

$$
\begin{bmatrix}
\delta x_\mathrm{E} \\
\delta y_\mathrm{E} \\
\delta {\phi}_\mathrm{E}
\end{bmatrix}
= \boldsymbol{J}
\begin{bmatrix}
\delta {\theta_1} \\
\delta {\theta_2} \\
\delta {\theta_3}
\end{bmatrix}
$$

以上が，各関節変位から先端の変位・姿勢を求める[順運動学](_Word/forward-kinematics.md)．  

### 逆運動学
逆に，先端の微小変位から各関節の微小変位を求めるには，ヤコビ行列の逆行列を用いる．   
※式($*$)は，微分逆運動学（速度レベルの逆問題）であり，「[逆運動学](_Word/inverse-kinematics.md)」そのものとは区別される．

$$
\begin{bmatrix}
\delta {\theta_1} \\
\delta {\theta_2} \\
\delta {\theta_3}
\end{bmatrix}
= \boldsymbol{J}^{-1}
\begin{bmatrix}
\delta x_\mathrm{E} \\
\delta y_\mathrm{E} \\
\delta {\phi}_\mathrm{E}
\end{bmatrix} \tag{$*$}
$$


- 解析的解法：幾何学的関係・三角関数の逆関数を用いて，閉じた式で関節角度を直接求める．
	- ↑ロボットの構成によっては解析解がありそのまま解ける  
- 数値解法：ヤコビ行列の逆行列を用いて微小変位を反復的に更新


[^1]: 鈴森康一．ロボット機構学．コロナ社（2004），p.129-130．