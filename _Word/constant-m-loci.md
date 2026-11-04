---
time: 2026-11-05T01:53
jp: 等M軌跡
en: Constant-M Loci
aliases:
  - 等M曲線
  - M円
  - 等M円
  - Constant-M Circles
  - Constant-M Locus
tags:
  - 分野/制御工学/古典制御
  - 要素/モデル・数式
up:
  - "[[_Word/frequency-response-analysis|周波数応答解析]]"
sibling:
  - "[[_Word/constant-n-loci|等N曲線]]"
  - "[[_Word/nichols-chart|ニコルス線図]]"
  - "[[_Word/magnitude-phase-plot|ゲイン位相線図]]"
pair:
  - "[[_Word/constant-n-loci|等N軌跡]]"
person:
source:
  - https://www.jstage.jst.go.jp/article/sicejl1954/1/3/1_3_159/_pdf/-char/en
---
# 等M軌跡／等M円（Constant-M Loci／Constant-M Circle）
> 直結フィードバック系において，閉ループ伝達関数の大きさ $M = |M(j\omega)|$ が一定の値をとる点を，開ループ周波数伝達関数 $G(j\omega)$ の平面上で結んだ曲線．

<img src="../_A/ext/2026/11/202611_055043_constant-m-loci.webp" alt="[外部著作物のため非公開]" width="400">  

$\mathrm{Fig}. 1$　等M円（ $G(j\omega)$平面 ）


<img src="../_A/ext/2026/11/202611_055855_constant-m-loci.webp" alt="[外部著作物のため非公開]" width="400">  

$\mathrm{Fig}. 2$　等M軌跡（ ゲイン位相平面．ニコルス線図 ）

## 注意点
### 前提：直結FB
直結フィードバック(Unity Feedback)とは，フィードバック経路の伝達関数 $H(s) = 1$ である系のこと．  

- $G(s)$：まっすぐ部分
- $H(s)$：ぐるっと部分

### 形状
座標系によって形状・呼び方が変わる（いずれも閉曲線）  

- $G(j\omega)$-plane：円（等M円）
- ゲイン位相線図：円ではない（等M軌跡）

---

## 導出
直結フィードバック系の閉ループ伝達関数 $M(s)$ は，$H(s) = 1$ であるから，  

$$
\boldsymbol{M}(s) = \frac{\boldsymbol{G}(s)}{1 + \boldsymbol{G}(s)\boldsymbol{H}(s)} = \frac{\boldsymbol{G}(s)}{1 + \boldsymbol{G}(s)}
$$

であり，$G(j\omega) = x + jy$  とおくと...  
閉ループの大きさは次のようになる．  

$$
M = |M(j\omega)| = \frac{\sqrt{x^2 + y^2}}{\sqrt{(1 + x)^2 + y^2}}
$$

両辺を二乗して整理すると，円の方程式となる．  

$$
\left( x - \frac{M^2}{1 - M^2} \right)^2 + y^2 = \left( \frac{M}{1 - M^2} \right)^2
$$

### ★中心

$$
\left( \frac{M^2}{1 - M^2}, \;\; 0 \right)
$$

### ★半径

$$
\left| \frac{M}{1 - M^2} \right|
$$

---

## 円の族の性質
★Mの値を変えることで，円の族＊が描かれる．  
第一に，円の族は $M = 1$ の直線(縦)と実軸に対して線対称．  

| Mの値     | 性質                                                                              |
| ------- | ------------------------------------------------------------------------------- |
| $M < 1$ | ・$M = 1$ の直線より右側の円<br>・$M \to 0$ で原点に縮む                                         |
| $M = 1$ | 直線 $x = - 1/2$<br>虚軸に平行な直線となる                                                   |
| $M > 1$ | ・$M = 1$ の直線より左側の円<br>・$M$ が大きいほど円が小さくなる<br>・$M \to \infty$ で $(-1,\; j0)$ 点に縮む |

## 使い方と読取り方
> ベクトル軌跡と一緒に等M軌跡をプロットすることで，閉ループ特性が分かる

- ベクトル軌跡と等M曲線の交点：その周波数における閉ループの大きさがMである
- 共振ピーク $M_r$：軌跡に接する円のうち，半径が最小(Mが最大)のものの(Mの)値
- 共振周波数 $\omega_r$：↑その接点における $\omega$
- 帯域幅 $\mathrm{BW}$：軌跡が $M - 0.707$ の円と交わる点の周波数  

## メモ  
- 「共振ピークをある値以下に抑えたい」ときは...
	- $G(j\omega)$ の規制が対応する等M軌跡と交わらず，かつ
	- 臨界点を囲まない　ようにする  

- ループゲインをあげると，より小さい(Mの大きい)園医接するようになり，共振ピークが大きくなってしまう  

- 径が不安定の時，共振ピークは意味を持たない．
	- →すなわち等M軌跡も意味を持たない．