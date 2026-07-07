---
time: 2026-07-07T23:32
jp: 冪等性
en: Idempotence
aliases:
  - "冪等性"
  - "べきとうせい"
  - "巾等性"
  - "等冪性"
  - "Idempotency"
tags:
  - 分野/数学
  - 分野/情報工学
  - 要素/概念
up:
  - "[[_Word/abstract-algebra|抽象代数学]]"
sibling:
  - "[[_Word/commutativity|可換性]]"
  - "[[_Word/associativity|結合性]]"
pair:
person:
  - "[[_Name/benjamin-peirce|ベンジャミン・パース]]"
source:
  - "https://ja.wikipedia.org/wiki/冪等"
---
# 冪等性（べきとうせい, Idempotence）
> ある操作を1回行っても複数回行っても結果が同じになる性質．

## 語源
ラテン語の idem （同じ）と，potere（冪）．  
## 2つの定義
### ①単項演算の冪等性
関数 $f$ に対して $f(f(x)) = f(x)$ が成り立つこと．  
例）絶対値関数 $|x|$ ← $||x|| = |x|$
### ②二項演算における冪等元
ある元 $x$ が $x * x = x$ を満たすとき，冪等元と呼ばれる．  
例）実数の乗算においては，$0$ と $1$ のみが該当．  
## 冪等である例
- GET，PUT，DELETE メソッド
	- ↑何回リクエストしてもリソースの最終状態が同じ
## 冪等でない例
- POST メソッド
	- ↑リクエストの旅にリソースが新規作成される可能性がある