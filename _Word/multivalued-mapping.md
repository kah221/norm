---
time: 2026-07-09T23:35
jp: 多価写像
en: Multivalued Mapping
aliases:
  - 多価写像
  - 多価関数
  - Multivalued Function
  - 多価函数
tags:
  - 分野/数学
  - 分野/数学/解析学
  - 要素/概念
up:
  - "[[_Word/set-theory|集合論]]"
sibling:
pair:
  - "[[_Word/mapping|1価写像]]"
person:
  - "[[_Name/bernhard-riemann|ベルンハルト・リーマン]]"
source:
  - https://ja.wikipedia.org/wiki/多価関数
---
# 多価写像（Multivalued Mapping）
> 1つの入力に対して複数の出力が対応しうる対応規則．厳密には写像の定義（1入力1出力）を満たさないが，定義を拡張して写像の枠組みで扱う．

[写像](_Word/mapping.md)は「1入力1出力」だが，多価写像ではこの制約が緩和され，1入力に対して複数の出力値が許される．  

多価関数を1価関数として取り扱うための方法  
- 「主値」の選定：定義域を制限して1つの値のみを選ぶ
- リーマン面の導入：...  

## 制御工学に関連して
[逆運動学](_Word/inverse-kinematics.md)は，  
- 手先位置空間から関節位置空間への多価写像となっている．
- （1つの手先位置に対して，複数の関節角度の解が存在しうる）
	- ↑非冗長マニピュレータであっても，複数解は存在しうる
	- （冗長マニピュレータなら，無限個）