---
time: 2026-07-12T16:47
jp: 位相進み要素
en: Lead Compensator
aliases:
  - 位相進み要素
  - 位相進み補償器
  - 位相進み補償
  - Phase Lead Compensator
tags:
  - 分野/制御工学/古典制御
  - 要素/手法・アルゴリズム
up:
  - "[[_Word/compensator|補償器]]"
sibling:
  - "[[_Word/lag-compensator|位相遅れ要素]]"
  - "[[_Word/lead-lag-compensator|位相進み遅れ要素]]"
  - "[[_Word/pid-controller|PID制御器]]"
pair:
  - "[[_Word/lag-compensator|位相遅れ要素]]"
person:
  - "[[_Name/hendrik-bode|ヘンドリック・ボーデ]]"
source:
  - http://www.ctleec.sakura.ne.jp/2023/01/21/30-位相進み補償器/
---
# 位相進み要素（Lead Compensator）
> 零点が極よりも原点に近い位置にある1次の有理伝達関数で，零点と極の間の周波数帯域において位相を進める特性を持つ要素．．

伝達関数は $\alpha > 1$ として

$$
C(s) = \frac{K(1 + \alpha T s)}{1 + Ts}
$$

零点 $s = -1/\alpha T$ が，極 $s = -1/T$ よりも原点に近いため，両者の間の周波数帯域で  
- ゲインが増加し，
- 位相が進む  

## 量
- 位相が最大に進む角周波数：$\omega_m = 1/(T \sqrt{\alpha})$    
- 最大位相進み量：$\phi_m = (\alpha - 1)/(\alpha + 1)$  
	- ↑$\alpha$ が大きいほど，進み量が増え，高周波域のゲインも $\alpha$ 倍に増加する．

## 制御系設計
位相進み要素を，制御系に直列に挿入する
- 目的：位相余裕の改善，安定性と即応性の改善
- 効果：ゲイン公差周波数付近の位相余裕が増大する

（位相遅れ要素は，低周波ゲインの増大による定常偏差改善を目的）


|        | 目的     |
| ------ | ------ |
| 位相進み要素 | 位相余裕改善 |
| 位相遅れ要素 | 定常偏差改善 |



