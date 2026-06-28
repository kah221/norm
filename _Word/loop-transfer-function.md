---
time: 2026-06-26T01:54
jp: 一巡伝達関数
en: Loop Transfer Function
aliases:
  - 一巡伝達関数
  - L(s)
tags:
  - 分野/制御工学/古典制御
  - 要素/モデル・数式
up:
  - "[[_Word/transfer-function|伝達関数]]"
  - "[[_Word/feedback-control-system|フィードバック制御系]]"
sibling:
  - "[[_Word/closed-loop-transfer-function|閉ループ伝達関数]]"
  - "[[_Word/open-loop-transfer-function|開ループ伝達関数]]"
pair:
  - "[[_Word/closed-loop-transfer-function|閉ループ伝達関数]]"
person:
  - "[[_Name/harry-nyquist|ハリー・ナイキスト]]"
  - "[[_Name/hendrik-bode|ヘンドリック・ボーデ]]"
source:
  - https://controlabo.com/open-loop-closed-loop/
---
# 一巡伝達関数（Loop Transfer Function, L(s)）
> フィードバック系においてループをある点で切り開き，そこに試験信号を入れてループを一巡させたときの入出力比．

制御器 $C(s)$ ，制御対象 $P(s)$ ，フィードバック要素 $H(s)$ で表すと
$$
L(s) = C(s)P(s)H(s)
$$
となる．  

次のような周波数領域での安定解析でよく使われる  
- ナイキスト安定判別法
- ボード線図
- 位相余裕
- ゲイン余裕
理由は，閉ループ伝達関数よりも，一巡伝達関数を用いる方が計算・設計が容易であるから．  

特に，$H(s) = 1$ の「ユニティフィードバック」の場合は，  
→「一巡伝達関数」=「開ループ伝達関数」 となるので，  
書籍では「開ループ伝達関数（一巡伝達関数）」としばしば表記される．