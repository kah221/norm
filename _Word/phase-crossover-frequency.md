---
time: 2026-07-14T01:11
jp: 位相交差周波数
en: Phase Crossover Frequency
aliases:
  - "位相交差周波数"
tags:
  - 分野/制御工学/古典制御
  - 要素/指標
up:
  - "[[_Word/bode-diagram|ボード線図]]"
sibling:
  - "[[_Word/gain-crossover-frequency|ゲイン交差周波数]]"
pair:
  - "[[_Word/gain-crossover-frequency|ゲイン交差周波数]]"
person:
  - "[[_Name/hendrik-bode|ヘンドリック・ボーデ]]"
source:
  - "https://controlabo.com/stability-margin/"
---
# 位相交差周波数（Phase Crossover Frequency, $\omega_{cp}$, $\omega_Q$）
> 開ループ伝達関数の位相が $-180 \: \mathrm{deg}$ となる角周波数．

## 性質
- [ゲイン余裕](_Word/gain-margin.md) = 位相交差周波数におけるゲインの符号を反転させたもの
- 位相交差周波数が $-180 \: \mathrm{deg}$ であることは
	- FB信号が入力と完全に同位相であることを意味し，
	- この周波数でゲインが $0 \: \mathrm{dB}$  以上であれば，正帰還ループにより信号が増幅され続けシステムが不安定化する．
- ★**有限の**位相交差周波数 $\omega_{cp}$ が存在しなければ，ゲイン余裕は $\infty$  

## 読み取り
### ボード線図
位相線図において，位相曲線が $-180 \: \mathrm{deg}$ の水平線と交わる周波数
### ナイキスト線図
ベクトル軌跡と実軸との交点 $\mathrm{Q}$ における周波数