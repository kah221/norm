---
time: 2026-07-09T22:59
jp: 2次遅れ系
en: Second-Order Lag System
aliases:
  - "2次遅れ系"
  - "2次遅れ要素"
  - "二次遅れ系"
tags:
  - 分野/制御工学/古典制御
  - 分野/信号処理
  - 要素/モデル・数式
up:
  - "[[_Word/transfer-function|伝達関数]]"
sibling:
  - "[[_Word/first-order-lag-system|1次遅れ系]]"
  - "[[_Word/dead-time|むだ時間]]"
pair:
person:
source:
  - "https://controlabo.com/second-order-system-impulse-step-response/"
---
# 2次遅れ系（Second-Order Lag System）
> 伝達関数の特性多項式が2次であり，固有振動数 $\omega_n$ と減衰比 $zeta$ の2つのパラメータで応答特性が決まるシステム．

## 伝達関数
（$\zeta$ と $\omega_n$ を用いた標準系）  

$$
G(s) = \frac{K \omega_n^2}{s^2 + 2 \zeta \omega_n + \omega_n ^2}
$$

- $K$：ゲイン
- $\zeta$：減衰比（減衰係数）
- $\omega_n$：固有角周波数 $[ \mathrm{rad} ]$  

## 特徴
- 1次遅れ系は，極を1つ持ち，単調に収束する挙動
- 2次遅れ系は，極を2つ持ち，単調には収束しない
- $\zeta$ の値によって応答の仕方に名前が付けられている
### 周波数応答
- 固有振動数 $\omega_n$ 付近に共振ピークが現れる
- $\zeta$ が小さいほどピークが鋭くなる
- 高周波域では
	- ゲイン： $-40 \: [ \mathrm{dB/dec}]$ で降下
	- 位相：$-180 \: [ \mathrm{deg} ]$ に近づく  
	- ↑これは1次遅れ系の2倍
## 例
：ばね-マス-ダンパ系
運動方程式は，  

$$
\begin{align}
m \ddot{x} + c \dot{x} + kx = u(t) \\
\omega_n = \sqrt{\frac{k}{m}} \\
\zeta = \frac{c}{2\sqrt{mk}}
\end{align}
$$


## $\zeta$ の値による分類
### $0 < \zeta < 1$：不足制動（不足減衰）
- 振動しながら収束
### $\zeta = 1$：臨界制動（臨界減衰）
- 振動せずに最もはやく収束
### $\zeta > 1$：過制動（過減衰）
- 振動無しだが収束が遅い
### $\zeta = 0$：持続振動(=臨界安定)

## 制御設計
で適切とされる減衰比の値  
- サーボ系で，$\zeta = 0.6 \: ～ \: 0.8$ 
- プロセス制御で，$\zeta = 0.2 \: ～ \: 0.4$ 