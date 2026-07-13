---
time: 2026-07-10T10:06
jp: リカッチ代数方程式
en: Algebraic Riccati Equation
aliases:
  - "リカッチ代数方程式"
  - "ARE"
  - "代数リカッチ方程式"
  - "リッカチ代数方程式"
tags:
  - 分野/制御工学/現代制御
  - 分野/数学/線形代数
  - 要素/モデル・数式
up:
  - "[[_Word/riccati-equation|リカッチ方程式]]"
sibling:
  - "[[_Word/differential-riccati-equation|微分リカッチ方程式]]"
  - "[[_Word/lyapunov-equation|リアプノフ方程式]]"
pair:
  - "[[_Word/differential-riccati-equation|微分リカッチ方程式]]"
person:
  - "[[_Name/suguru-arimoto|有本 卓]]"
  - "[[_Name/david-potter|デイヴィッド・ポッター]]"
source:
  - "https://qiita.com/GANTZ/items/c9fffa240648ace1d717"
---
# リカッチ代数方程式（Algebraic Riccati Equation, ARE）
> 微分リカッチ方程式の定常解（時間微分項をゼロとおいた形）として得られる，行列 $P$ に関する2次の代数方程式．

## 標準形
連続時間系における標準形は  

$$
\boldsymbol{A}^{\top} \boldsymbol{P} + \boldsymbol{PA} - \boldsymbol{PBR^{-1}B^{\top}P + Q} = \boldsymbol{0}
$$

$A$：システム行列  
$B$：入力行列  
$Q$：状態に対する重み行列（半正定）  
$R$：入力に対する重み行列（正定）  
$P$：未知変数（正定対称行列）  

有限時間最適制御で現れる，微分リカッチ方程式（DRE）において終端時刻を無限大にすると，$P(t)$ が定常地に収束し，その収束先がAREの解になる．  
この収束が保証されるための条件は $(A, B)$ が可安定（←可制御であれば十分）であること．  
離散時間系にも対応する「離散リカッチ代数方程式（DARE）」もある．

## 2次形式評価関数 $J$ を最小にする問題[^1]
2次形式評価関数 $J$  

$$
J = \int_0^\infty \{ \boldsymbol{x}^{\top}(t) Q \boldsymbol{x}(t) + ru^2(t)\} \, \mathrm{d}t
$$

を最小にする最適制御則は次で与えられる

$$
u(t) = -\boldsymbol{r}^{-1} \boldsymbol{b}^{\top}P \boldsymbol{x}(t) \tag{$*$}
$$

★この $P$ はリカッチ代数方程式を満たす正定行列である．

$$
A^{\top} P + PA - P \boldsymbol{b} r^{-1}\boldsymbol{b}^{\top} P + Q = \boldsymbol{O}
$$

なお，式 ($*$) は，状態フィードバックベクトル $\boldsymbol{f}$ を $\boldsymbol{f} =r^{-1}\boldsymbol{b}^{\top} P$ とした状態フィードバック制御則であり，式($*$) を適用した閉ループシステムは必ず安定となることが保証される[^2]．
## 出てくる場所
AREの解$P$ はLQRでは，
- 最適フィードバックゲイン $K = R^{-1}BTP$ の算出で使用する．  
カルマンフィルタでは，
- 双対なAREを解いてオブザーバゲインの算出する際に使用される．
## 代表的な解法
有本-ポッター法：ハミルトン行列の固有値分解を利用する
## MATLAB実装
- `lqr`
- `care`
- `dare` ←離散時間系に対応する
- ↑いずれも有本-ポッター法を内部で実装


[^1]: 佐藤和也，下本陽一，熊澤典良．はじめての現代制御理論．改訂第2版，講談社（2022），p.213．
[^2]: 森泰親．演習で学ぶ現代制御理論．新装版，森北出版（2014）．