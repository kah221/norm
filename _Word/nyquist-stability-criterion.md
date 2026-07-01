---
time: 2026-07-02T05:46
jp: ナイキストの安定判別法
en: Nyquist Stability Criterion
aliases:
  - "ナイキストの安定判別法"
  - "ナイキスト安定判別法"
  - "Nyquist Criterion"
tags:
  - 分野/制御工学/古典制御
  - 要素/定理・法則
up:
  - "[[_Word/stability-analysis|安定性解析]]"
sibling:
  - "[[_Word/bode-diagram|ボード線図]]"
  - "[[_Word/root-locus|根軌跡]]"
  - "[[_Word/routh-hurwitz-stability-criterion|ラウス・フルビッツの安定判別法]]"
pair:
person:
  - "[[_Name/harry-nyquist|ハリー・ナイキスト]]"
source:
  - "https://controlabo.com/nyquist-stability-criterion/"
---
# ナイキストの安定判別法（Nyquist Stability Criterion）
> フィードバック制御系の閉ループ安定性を，一巡伝達関数 $L(s)$ のナイキスト線図と臨界点 $(−1, j0)$ の周回数から図式的に判別する手法．

## 判定手順
1. ナイキスト経路を $s$平面にプロット
	- 開ループ極を求める
	- 開ループ零点を求める
	- 虚軸上の極を求める
	- RHPの極の数 $P$ をカウントする
		- この段階で，安定条件の公式 $N = Z - P$ と，目当ての「閉ループ安定」の条件 $Z = 0$ から，所望の $N$ の値が分かる．
2. ナイキスト線図を $L(s)$平面にプロット（ゲインは $K = 1$ に仮置き）
	- ①虚軸の上半分 $(0 < \omega < + \infty)$　←これはベクトル軌跡そのもの
	- ②虚軸の下半分 $(- \infty < \omega < 0)$　←これは①の実軸対象
	- ③無限大半円 $(s = R e ^{j\theta}, \theta: +90 → -90, R → \infty)$ あるいは $(|s| → \infty)$　←厳密にプロパーのとき原点の「点」となる
	- ④迂回用の小半円 $(s = \epsilon e ^{j\theta}, \theta: +90 → -90, \epsilon → 0)$　←無限大半円となる
3. ナイキスト線図が臨界点$(-1, j0)$ を"包囲"する回数 $N$ を読み取る
	- ①+②+③+④がそのままナイキスト線図となり，組み合わせることで **閉曲線** となる
	- 臨界点を包囲する回数 $N$ が，所望の値
		- であれば，「閉ループ安定」となる
		- なければ，「閉ループ安定」でない

## 例題（手書きノート）
一巡伝達関数 $L(s)$ が次式で与えられる一般的なシステムに対して，「閉ループ安定性」を判別する．  
注意）一巡伝達関数は閉ループ部分も含めた入出力比のこと．  
ナイキスト安定判別法では，「閉ループ極」の位置を特定せずに安定判別することができる．（画像1枚目冒頭で求めている極と零点は，開ループ極であって閉ループ極ではない．）

$$
L(s) = \frac{K}{s(s+1)}
$$

<img src="../_A/own/2026/07/202607_024723_nyquist-stability-criterion.webp" alt="" width="400">
<img src="../_A/own/2026/07/202607_024734_nyquist-stability-criterion.webp" alt="" width="400">
<img src="../_A/own/2026/07/202607_024742_nyquist-stability-criterion.webp" alt="" width="400">
<img src="../_A/own/2026/07/202607_024747_nyquist-stability-criterion.webp" alt="" width="400">