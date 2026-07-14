---
time: 2026-07-14T16:27
jp: ラプラス変換
en: Laplace Transform
aliases:
  - ラプラス変換
  - L
  - Laplace Transformation
tags:
  - 分野/数学/解析学
  - 分野/制御工学/古典制御
  - 分野/信号処理
  - 要素/手法・アルゴリズム
up:
  - "[[_Word/integral-transform|積分変換]]"
sibling:
  - "[[_Word/fourier-transform|フーリエ変換]]"
  - "[[_Word/z-transform|z変換]]"
pair:
  - "[[_Word/inverse-laplace-transform|逆ラプラス変換]]"
person:
  - "[[_Name/pierre-simon-laplace|ピエール＝シモン・ラプラス]]"
  - "[[_Name/oliver-heaviside|オリヴァー・ヘヴィサイド]]"
source:
  - https://controlabo.com/laplace-transform/
---
# ラプラス変換（Laplace Transform, L）
> 時間領域の関数 $f(t)$ を，複素変数 $s$ の関数 $F(s)$ に変換する積分変換．微分方程式を代数方程式に変換する．

## 定義
$s = \sigma + j\omega$ として，
$$
F(s) = \int_0^\infty f(t)e^{-et}\: \mathrm{d}t
$$

## メモ
- 利点：微分方程式を代数方程式に変換できる
- 時間領域における
	- 微分は，$s$ の乗算になる
	- 積分は，$s$ の除算になる
- 運動方程式や回路方程式をラプラス変換で伝達関数にできる
- フーリエ変換の変数 $j\omega$ を複素数 $s = \sigma + j\omega$ に拡張したものとみなすことができる
	- 実部 $\sigma$ の導入により，フーリエ変換では収束しない関数にも適用可能となった
- 流れ
	- 「運動方程式（微分方程式）」
	- ↓＜ラプラス変換＞
	- 「伝達関数（代数方程式）」
	- ↓＜$s = j\omega$ 代入＞
	- 「周波数伝達関数（代数方程式）」

## 変換表[^1]

| No. | $f(t)$                              | $F(s)$                              | Memo      |
| --- | ----------------------------------- | ----------------------------------- | --------- |
| 1   | $$\delta(t)$$                       | $$1$$                               | デルタ関数     |
| 2   | $$u_s(t) = 1$$                      | $$\frac{1}{s}$$                     | 単位ステップ関数  |
| 3   | $$u_l(t) = t$$                      | $$\frac{1}{s^2}$$                   | 単位ランプ関数   |
| 4   | $$e^{-at}$$                         | $$\frac{1}{s+a}$$                   | 2の $s$ 推移 |
| 5   | $$te^{-at}$$                        | $$\frac{1}{(s+a)^2}$$               | 3の $s$ 推移 |
| 6   | $$\mathrm{sin}\:\omega t$$          | $$\frac{\omega}{s^2+\omega^2}$$     |           |
| 7   | $$\mathrm{cos}\:\omega t$$          | $$\frac{s}{s^2+\omega^2}$$          |           |
| 8   | $$e^{-at}\:\mathrm{sin}\:\omega t$$ | $$\frac{\omega}{(s+a)^2+\omega^2}$$ | 6の $s$ 推移 |
| 9   | $$e^{-at}\:\mathrm{cos}\:\omega t$$ | $$\frac{s+a}{(s+a)^2+\omega^2}$$    | 7の $s$ 推移 |
| 10  | $$\frac{t^n}{n!}$$                  | $$\frac{1}{s^{n+1}}$$               |           |
## 性質[^1]
### $t$ 領域での微分
微分しない状態で変換し， $s$ を掛け，初期値を引く  
$$
\mathcal{L}\{ f'(t) \} = s F(s) - f(0)
$$

### $t$ 領域での積分
積分しない状態で変換し， $\frac{1}{s}$ を掛ける  
$$
\mathcal{L} \left[ \int_0^t f(\tau) \mathrm{d}t \right] = \frac{1}{s}F(s)
$$

### $s$ 領域での推移
$s$ 領域での推移とは，変換後の関数 $F(s)$ で，$s$ に何かを足したり引いたりする操作．  
これは，時間領域関数 $f(t)$ において， $e^{at}$ の掛算に相当する．（足し引きの符号反転に注意）  
$$
\mathcal{L} \left[ e^{at}f(t) \right] = F(s-a)
$$

### $t$ 領域での推移
$t$ 領域での推移とは，時間領域関数 $f(t)$ で，$t$ に何かを足したり引いたりする操作．  
これは，変換後の関数 $F(s)$ で，$e^{-as}$ の掛算に相当する．  
$$
\mathcal{L}\left[ f(t-a) \right] = e^{-as}F(s)
$$
ただし，$f(t-a) = 0 \:\: (0 < t < a)$  
### 最終値定理
$sF(s)$ が安定の場合のみ，次が成り立つ  
$$
\lim_{t \to \infty} f(t) = \lim_{s \to 0}sF(s)
$$

### 合成積, 畳み込み積分
$$
\mathcal{L} \left[ \int_0^t f(t-\tau)g(\tau) \: \mathrm{d}t \right] = F(s)G(s)
$$


[^1]: 佐藤和也，平元和彦，平田研二．はじめての制御工学．改訂第2版，講談社（2023），p.45-47．