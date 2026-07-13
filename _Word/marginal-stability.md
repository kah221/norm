---
time: 2026-07-05T02:50
jp: 臨界安定
en: Marginal Stability
aliases:
  - 臨界安定
  - 安定限界
  - Critical Stability
tags:
  - 分野/制御工学/古典制御
  - 分野/制御工学/現代制御
  - 要素/概念
up:
  - "[[_Word/stability|安定性]]"
sibling:
  - "[[_Word/asymptotic-stability|漸近安定]]"
  - "[[_Word/open-loop-stability|開ループ安定性]]"
  - "[[_Word/closed-loop-stability|閉ループ安定性]]"
pair:
person:
  - "[[_Name/aleksandr-lyapunov|アレクサンドル・リアプノフ]]"
source:
  - https://controlabo.com/stability/
---
# 臨界安定（Marginal Stability）
> システムの極が虚軸上に存在し，応答が減衰も発散もせず持続振動する安定性の境界状態．

漸近安定と不安定の教会に当たる状態．  
極が虚軸上にあるため，インパルス王党派一定振幅の持続振動となる．  
僅かなゲイン変化で安定にも不安定にもなりうるため，設計上は避けるべき状態．  

典型例：摩擦や空気抵抗がない理想的なばねマス系  

リアプの負の意味では安定（有界）だが，漸近安定ではない．  
BIBO安定（有界入力有界出力安定）も一般的には保証されない．  

★ナイキスト安定判別法では，ナイキスト線図が臨界点 $(-1, j0)$ を丁度通過する状態に対応する．  