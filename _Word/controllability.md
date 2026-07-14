---
time: 2026-07-14T10:39
jp: 可制御性
en: Controllability
aliases:
  - 可制御性
tags:
  - 分野/制御工学/現代制御
  - 要素/概念
up:
  - "[[_Word/state-space-representation|状態空間表現]]"
sibling:
  - "[[_Word/observability|可観測性]]"
  - "[[_Word/stabilizability|可安定性]]"
pair:
  - "[[_Word/observability|可観測性]]"
person:
  - "[[_Name/rudolf-kalman|ルドルフ・カルマン]]"
source:
  - https://blog.control-theory.com/entry/2024/01/29/154815
---
# 可制御性（Controllability）
> 任意の初期状態から，適切な入力を加えることで，有限時間内に任意の目標状態へ移すことができるシステムの性質．

状態方程式 $\boldsymbol{\dot{x}} = \boldsymbol{Ax} + \boldsymbol{Bu}$ ，出力方程式 $\boldsymbol{y} = \boldsymbol{Cx} + \boldsymbol{Du}$ で記述される，$n$ 次元[線形時不変](_Word/linear-time-invariant.md)系において，  
可観測性は行列 $\boldsymbol{A}$ と $\boldsymbol{B}$ のみで決まる．（$\boldsymbol{C}$ には依存しない）    

## 性質
- 可制御である ⇔ 状態FBによる閉ループ極を任意の位置に設定できること
	- ↑必要十分条件
- LQRの設計においても代数リカッチ方程式の正定対称解が存在するための条件となる
- [可観測性](_Word/observability.md)との間に双対性が成り立つ
	- $(\boldsymbol{A}, \boldsymbol{B})$ が可制御であることと，$(\boldsymbol{B}^\top, \boldsymbol{A}^\top)$ が可観測であること は同値

## 判定
可制御性行列 $\boldsymbol{U}_c$ の階級が
- $n$ であれば，可制御
- $n$ 未満であれば，不可制御