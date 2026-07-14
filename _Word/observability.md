---
time: 2026-07-14T10:40
jp: 可観測性
en: Observability
aliases:
  - "可観測性"
tags:
  - 分野/制御工学/現代制御
  - 要素/概念
up:
  - "[[_Word/state-space-representation|状態空間表現]]"
sibling:
  - "[[_Word/controllability|可制御性]]"
  - "[[_Word/detectability|可検出性]]"
pair:
  - "[[_Word/controllability|可制御性]]"
person:
  - "[[_Name/rudolf-kalman|ルドルフ・カルマン]]"
source:
  - "https://blog.control-theory.com/entry/2024/01/29/154815"
---
# 可観測性（Observability）
> 有限時間にわたる入力と出力の観測のみから，システムの初期状態をすべて一意に決定できるシステムの性質．

状態方程式 $\boldsymbol{\dot{x}} = \boldsymbol{Ax} + \boldsymbol{Bu}$ ，出力方程式 $\boldsymbol{y} = \boldsymbol{Cx} + \boldsymbol{Du}$ で記述される，$n$ 次元[線形時不変](_Word/linear-time-invariant.md)系において，  
可観測性は行列 $\boldsymbol{A}$ と $\boldsymbol{C}$ のみで決まる．（$\boldsymbol{B}$ には依存しない）  

## 性質
- 可観測 ⇔ オブザーバのゲイン行列 $\boldsymbol{L}$ を設計して推定誤差のダイナミクス $(\boldsymbol{A} - \boldsymbol{LC})$ の固有値を任意に配置可能
	- ↑必要十分条件
- [可制御性](_Word/controllability.md)との間には双対性が成り立つ
	- $(\boldsymbol{C}, \boldsymbol{A})$ が可観測であることと，$(\boldsymbol{A}^\top, \boldsymbol{C}^\top)$ が可制御であること は同値

## 判定
可観測性行列 $\boldsymbol{U}_o$ の階級が  
- $n$ であれば，可観測
- $n$ 未満であれば，不可観測