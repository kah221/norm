---
time: 2026-07-14T16:20
jp: 整定時間
en: Settling Time
aliases:
  - "整定時間"
  - "セトリングタイム"
tags:
  - 分野/制御工学/古典制御
  - 要素/指標
up:
  - "[[_Word/transient-response|過渡応答]]"
sibling:
  - "[[_Word/overshoot|オーバーシュート]]"
  - "[[_Word/rise-time|立ち上がり時間]]"
  - "[[_Word/delay-time|遅れ時間]]"
  - "[[_Word/damping-ratio|減衰比]]"
pair:
person:
source:
  - "https://controlabo.com/control-performance/"
---
# 整定時間（Settling Time）
> ステップ応答において，出力が最終値（定常値）の許容範囲（一般に ±2% or ±5%）に収まり，以後その範囲から出なくなるまでに要する時間．

許容範囲の基準は ±2% or ±5% が代表的（MATLABの`stepinfo`関数ではデフォルト 2%）  
整定時間とオーバーシュートにはトレードオフの関係があり，減衰比を小さくするとオーバーシュートは増大するが，振動が長引くため整定時間は短くなるとは限らない．