---
time: 2026-07-13T23:47
jp: ゲイン余裕
en: Gain Margin
aliases:
  - "ゲイン余裕"
  - "GM"
  - "利得余裕"
tags:
  - 分野/制御工学/古典制御
  - 要素/指標
up:
  - "[[_Word/stability-margin|安定余裕]]"
sibling:
  - "[[_Word/phase-margin|位相余裕]]"
pair:
  - "[[_Word/phase-margin|位相余裕]]"
person:
  - "[[_Name/hendrik-bode|ヘンドリック・ボーデ]]"
source:
  - "https://controlabo.com/stability-margin/"
---
# ゲイン余裕（Gain Margin, GM, $g_m$）
> 開ループ伝達関数の位相が $- 180 \: \mathrm{deg}$ となる位相交差周波数 $\omega_{cp}$ において，ゲインが $0 \: \mathrm{dB}$ からどれだけ余裕があるかを表す安定度指標．

## 性質
- ゲイン余裕が正：閉ループ安定
- ゲイン余裕が0：[安定限界](_Word/marginal-stability.md)
- ゲイン余裕が負：不安定
## 定義式①[^1]
[位相交差周波数](_Word/phase-crossover-frequency.md) $\omega_{cp}$ を用いて表すと，
$$
g_m = -g(\omega_{cp})
$$


## 定義式②[^1]
一巡周波数応答のベクトル軌跡が，負の実軸と交わる点を $\mathrm{Q}$ としたとき，線分 $\mathrm{OQ}$ の長さを用いて，
$$
g_m = 20 \: \mathrm{log}_{10} \: \frac{1}{\mathrm{OQ}} \: [\mathrm{dB}]
$$
あるいは $\mathrm{OQ}$ を周波数伝達関数から求めると，
$$
\begin{align*}
g_m = \{ \: 20 \: \mathrm{log}_{10} \: 1 \: \} - \{ \: 20 \: \mathrm{log}_{10} \: |G(j\omega_{cp})H(j\omega_{cp})| \: \} \\\\
= 20 \: \mathrm{log}_{10} \frac{1}{|G(j\omega_{cp})H(j\omega_{cp})|} \: [\mathrm{dB}]
\end{align*}
$$

## 推奨値
- サーボ系：12 ~ 20 $\mathrm{dB}$
- プロセス制御：3 ~ 10 $\mathrm{dB}$  

実測においては，[位相余裕](_Word/phase-margin.md)は比較的明確に得られるが，ゲイン余裕は高周波域でのノイズの影響により不鮮明になる場合がある．  
位相余裕とゲイン余裕合わせて安定余裕と呼ぶ．

## 読み取り
### ボード線図上では，
ゲイン余裕 $g_m$ は，位相線図が $-180 \: \mathrm{deg}$ を横切る周波数 $\omega_{cp}$ を読み取り，その周波数でのゲイン線図の値と $0 \: \mathrm{dB}$ の差
### ナイキスト線図上では，
ゲイン余裕 $g_m$ は，ベクトル軌跡が負の実軸と交わる点 $\mathrm{Q}$ の大きさの逆数に相当．

[^1]: 森泰親．演習で学ぶ現代制御理論．新装版，森北出版（2014），p.105-106．