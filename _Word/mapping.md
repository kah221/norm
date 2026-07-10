---
time: 2026-07-09T23:34
jp: 写像
en: Mapping
aliases:
  - 写像
  - Map
  - 1価写像
  - Single-Valued Mapping
tags:
  - 分野/数学
  - 要素/概念
up:
  - "[[_Word/set-theory|集合論]]"
sibling:
pair:
  - "[[_Word/multivalued-mapping|多価写像]]"
person:
source:
  - https://wiis.info/math/set/mapping/mapping/
---
# 写像（Maping）
> 2つの集合 A, B が与えられたとき，A の各元に対して B のただ1つの元を対応させる規則．

集合 $A$ の任意の元 $a$ に対して集合 $B$ の元 $b$ がただ1つ定まるとき，  
この対応規則 $f: A \: → \: B$   
を，$A$ から $B$ への写像と呼ぶ．  

## 名称対応
- $A$ ：始域（定義域）
- $B$ ：終域
- $a$ に対して定まる $b = f(a)$ を，「$a$ の像」 と呼ぶ．
## メモ
- 1つの入力に対して複数の出力が存在する対応は，写像の定義を満たさない．
- ↑この性質を強調するために「1価写像」と表記されることがある．
	- 写像は全て1価であるので，1価写像と写像は同義
## 制御工学に関連して
[ナイキスト安定判別法](_Word/nyquist-stability-criterion.md)では，  
- $s$平面上のナイキスト経路$\Gamma_s$ を，$L(s)$平面上へ写像することで，ナイキスト線図を得る．  

[順運動学](_Word/forward-kinematics.md)は，  
- 関節変位空間から，手先位置空間への写像．
- （1つの関節角度に対して，手先位置が1つに定まる←1価）