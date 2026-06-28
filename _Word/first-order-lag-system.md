---
time: 2026-06-25T02:31
jp: 1次遅れ系
en: First-Order Lag System
aliases:
  - 1次遅れ系
tags:
  - 分野/制御工学/古典制御
  - 分野/信号処理
  - 要素/モデル・数式
up:
  - "[[_Word/transfer-function|伝達関数]]"
  - "[[_Word/linear-time-invariant-system|線形時不変システム]]"
sibling:
  - "[[_Word/second-order-lag-system|2次遅れ系]]"
  - "[[_Word/integral-element|積分要素]]"
  - "[[_Word/proportional-element|比例要素]]"
  - "[[_Word/dead-time-element|無駄時間要素]]"
person:
  - "[[_Name/hendrik-bode|ヘンドリック・ボーデ]]"
source:
  - https://eng.kice.tokyo/control/delay-element/
---
# 1次遅れ系（First-Order Lag System）
> 伝達関数の最高次数が1であり，入力に対して出力が指数関数的に遅れて追従するシステム．

伝達関数は次式で表される．（$K$：ゲイン，$T$：時定数）
$$
G(s) = \frac{K}{Ts+1}
$$
特性方程式は $Ts + 1 = 0$ であり，極は $s = -\frac{1}{T}$ という実数の単極で，常に安定．  

## 周波数応答の観点  
低周波域
- ゲイン：水平
- 位相：$0$ 度
高周波域
- ゲイン：$-20 dB/dec$
- 位相：$-90$ 度に近づく
## 信号処理の分野
1次フィルタと等価  
実例
- RC積分回路
- 熱系
- モータの電気的ダイナミクス
- その他，より複雑なシステムの近似モデルとして