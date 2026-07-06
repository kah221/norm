---
time: 2026-07-07T02:09
jp: 因果フィルタ
en: Causal Filter
aliases:
  - 因果フィルタ
  - 因果的フィルタ
  - 因果システム
tags:
  - 分野/信号処理
  - 要素/概念
up:
  - "[[_Word/digital-filter|ディジタルフィルタ]]"
sibling:
  - "[[_Word/zero-phase-filtering|ゼロ位相フィルタリング]]"
pair:
  - "[[_Word/non-causal-filter|非因果フィルタ]]"
person:
source:
  - https://tech-introduction.com/ディジタル信号処理-安定性と因果性/
---
# 因果フィルタ（Causal Filter）
> 現在および過去の入力のみから出力を生成し，未来の入力を参照しないフィルタ．

[線形時不変系](_Word/linear-time-invariant.md)が因果的であるための必要十分条件は，インパルス応答 $h[n]$ が $n < 0$ で $h[n] = 0$ となること．  
↑これは，インパルス応答自体が因果的であるということ．  

現在の時刻で未来の入力を知ることは不可能であるから，物理的に実現可能なリアルタイムシステムは，必ず因果的．  

## 特徴
- 必然的に位相遅れを伴う
- 位相歪みをゼロにすることは不可能
- 