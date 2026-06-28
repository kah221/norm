---
time: 2026-06-26T02:13
jp: 閉ループ安定性
en: Closed-Loop Stability
aliases:
  - 閉ループ安定性
tags:
  - 分野/制御工学/古典制御
  - 要素/概念
up:
  - "[[_Word/stability|安定性]]"
sibling:
  - "[[_Word/open-loop-stability|開ループ安定性]]"
  - "[[_Word/internal-stability|内部安定性]]"
pair:
  - "[[_Word/open-loop-stability|開ループ安定性]]"
person:
  - "[[_Name/edward-routh|エドワード・ラウス]]"
  - "[[_Name/adolf-hurwitz|アドルフ・フルビッツ]]"
  - "[[_Name/harry-nyquist|ハリー・ナイキスト]]"
source:
  - https://controlabo.com/internal-stability/
---
# 閉ループ安定性（Closed-Loop Stability）
> フィードバックループを閉じた状態での制御系全体の安定性．閉ループ伝達関数の極がすべて複素平面の左半面に存在することが条件．

制御工学において，最終的に保証すべき安定性はこれ．（開ループ安定性ではない！）  
開ループ安定性とは独立した概念である．  
閉ループ系の特性方程式
$$
1 + C(s)P(s)H(s) = 0
$$
の根(=閉ループ極)が，全て左半平面にある時，閉ループ安定である．  

閉ループ伝達関数が安定であるだけでは不十分な場合もある...  
→内部安定性（外乱入力に対するシステム内部の信号も含めてすべてが安定であること）が要求される．  

## 閉ループ安定性の判定手法
- 根軌跡法
- ラウス・フルビッツの安定判別法
- ナイキストなんてい判別法
- ボード線図を用いた位相余裕・ゲイン余裕の評価
