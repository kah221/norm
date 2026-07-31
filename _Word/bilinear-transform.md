---
time: 2026-07-31T23:14
jp: 双一次変換
en: Bilinear Transform
aliases:
  - "双一次変換"
  - "双一次Z変換"
  - "タスティン変換"
  - "台形差分法"
  - "Tustin Transform"
  - "Trapezoidal Method"
tags:
  - 分野/信号処理
  - 分野/制御工学/古典制御
  - 要素/手法・アルゴリズム
up:
  - "[[_Word/z-transform|z変換]]"
sibling:
  - "[[_Word/laplace-transform|ラプラス変換]]"
pair:
person:
  - "[[_Name/arnold-tustin|アーノルド・タスティン]]"
source:
  - "https://ja.wikipedia.org/wiki/双一次変換"
---
# 双一次変換（Bilinear Transform）
> 連続時間領域におけるLTI系の伝達関数 $\boldsymbol{H}_a(s)$ を，離散時間領域における等価な伝達関数 $\boldsymbol{H}_d(z)$ に変換するために用いられる等角写像．

$s$ 平面上の虚軸を $z$ 軸平面上の単位円周に写像する変換．  
双一次変換は元のフィルタの安定性を保持する．  
→連続系で安定な系ならば、離散化後も安定  

安定：
- $s$ 平面上の左半面
- $z$ 平面上の単位円内部

## 変換式
$T$：サンプリング周期

$$
s = \frac{2}{T}・\frac{z-1}{z + 1}
$$

