---
time: 2026-07-14T15:52
jp: 減衰比
en: Damping Ratio
aliases:
  - 減衰比
  - 減衰係数比
  - 臨界減衰比
  - ダンピング比
tags:
  - 分野/機械力学
  - 要素/指標
up:
  - "[[_Word/second-order-lag-system|2次遅れ系]]"
sibling:
  - "[[_Word/natural-frequency|固有振動数]]"
  - "[[_Word/overshoot|オーバーシュート]]"
  - "[[_Word/settling-time|整定時間]]"
pair:
person:
source:
  - https://www.onosokki.co.jp/HP-WK/c_support/newreport/dampingfactor/dampingfactor_2.htm
---
# 減衰比（Damping Ratio, $\zeta$）
> 粘性減衰を有する振動系において，実際の減衰係数 c と臨界減衰係数 $c_c$ の比 $\zeta = c / c_c$．系が振動するか否かの境界を $1$ として正規化した無次元量．

質量 $m$ ，ばね定数 $k$ ，減衰係数 $c$ の1自由度振動系において，  
固有角振動数 $\omega_n$ ： $\omega_n = \sqrt{\frac{k}{m}}$  
臨界減衰係数 $c_c$ ： $c_c = 2 \sqrt{mk}$  ←振動と非振動の境界となる減衰係数  
減衰比 $\zeta$ ： $\zeta = \frac{c}{c_c} = \frac{c}{2\sqrt{mk}} = \frac{c}{2\omega_n}$ ←$c_c$ で正規化  

## 応答違い
正規化済みなので，1より大きいか小さいかで振動の有無が判別できる  
- $\zeta = 0$ ：無減衰（持続振動，[臨界安定](_Word/marginal-stability.md)）
- $0 < \zeta < 1$ ：不足減衰（振動しながら減衰）
- $\zeta = 1$ ：臨界減衰（振動せずに最も早く収束）
- $\zeta > 1$ ：過減衰（振動しないが，臨界減衰より収束が悪い）

## 2次遅れ系
2次遅れ系の伝達関数に $\zeta$ として含まれる．
- サーボ系では，$\zeta = 0.6 \: ～ \: 0.8$ が一般的な目標値
- $\zeta = 1/\sqrt{2} \approx 0.707$ は，オーバーシュートを許容しつつ，整定時間を最短に抑える実用的な最低値としてよく用いられる．