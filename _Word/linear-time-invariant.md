---
time: 2026-07-07T01:12
jp: 線形時不変
en: Linear Time-Invariant
aliases:
  - "線形時不変"
  - "LTI"
  - "線形時不変系"
  - "LTI System"
  - "線型時不変"
tags:
  - 分野/制御工学/古典制御
  - 分野/制御工学/現代制御
  - 分野/信号処理
  - 要素/概念
up:
  - "[[_Word/system-theory|システム理論]]"
sibling:
  - "[[_Word/nonlinear-system|非線形系]]"
  - "[[_Word/linear-time-varying-system|線形時変系]]"
pair:
person:
  - "[[_Name/norbert-wiener|ノーバート・ウィーナー]]"
source:
  - "https://ja.wikipedia.org/wiki/LTIシステム理論"
---
# 線形時不変（Linear Time-Invariant, LTI）
> 線形性と時不変性の2つの性質を同時に満たすシステム．

線形性：重ね合わせの原理が成立する  
時不変性：入力を時間方向にシフトしても出力が同じだけシフトするだけで，波形自体は変わらないこと  
制御工学，信号処理，電気回路の理論のほぼすべてはLTI系を前提としている．
## 性質
- システムの挙動がインパルス応答 $h(t)$ のみで完全に特徴づけられること．
- 任意の入力 $u(t)$ に対する出力は，畳み込み $y(t) = u(t) * h(t)$ で求められる