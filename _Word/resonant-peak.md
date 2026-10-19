---
time: 2026-10-12T03:44
jp: 共振ピーク
en: Resonant Peak
aliases:
  - "共振ピーク"
  - "M_r"
  - "共振ピーク値"
  - "共振値"
  - "Resonance Peak"
  - "Resonant Peak Magnitude"
tags:
  - 分野/制御工学/古典制御
  - 要素/指標
up:
  - "[[_Word/frequency-response-analysis|周波数応答解析]]"
sibling:
  - "[[_Word/damping-ratio|減衰比]]"
  - "[[_Word/phase-margin|位相余裕]]"
  - "[[_Word/gain-margin|ゲイン余裕]]"
  - "[[_Word/second-order-lag-system|2次遅れ系]]"
pair:
person:
source:
  - "https://zenn.dev/techneko/articles/51595917c3e85a"
---
# 共振ピーク（Resonant Peak, $M_r$）
> 周波数応答のゲイン曲線が示す最大値

2次遅れ系の標準形

$$
G(s) = \frac{\omega_n ^2}{s^2 + 2 \zeta \omega_n s + \omega_n ^2}
$$

では，ゲインが最大となる角周波数は，共振角周波数 $\omega_r = \omega_n \sqrt{1 - 2 \zeta^2}$ である．  
これは固有角周波数 $\omega_n$ とは一致しない．  

この周波数でのゲインが共振ピーク $M_r$ であり，次式で定義される．

$$
M_r = \frac{1}{2\zeta \sqrt{1 = \zeta^2}}
$$

なお，この式は $0 < \zeta < \frac{1}{\sqrt{2}}$ のときのみ成り立つ．  
減衰率 $\zeta$ が $1 / \sqrt2$ 以上のとき，共振ピークは無い．  

注意：共振ピークの定義は「閉ループゲインの絶対値の最大値」とする場合と，「直中ゲインで正規化した最大値」とする場合などがある．