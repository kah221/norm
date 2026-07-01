---
time: 2026-07-01T01:32
jp: ナイキスト経路
en: Nyquist Path
aliases:
  - ナイキスト経路
  - Nyquist Contour
  - ナイキスト閉曲線
tags:
  - 分野/制御工学/古典制御
  - 要素/概念
up:
  - "[[_Word/nyquist-plot|ナイキスト線図]]"
sibling:
  - "[[_Word/nyquist-stability-criterion|ナイキストの安定判別法]]"
  - "[[_Word/vector-locus|ベクトル軌跡]]"
pair:
person:
  - "[[_Name/harry-nyquist|ハリー・ナイキスト]]"
source:
  - https://controlabo.com/nyquist-stability-criterion/
---
# ナイキスト経路（Nyquist Path）
> 複素s平面の右半面（RHP）全体を囲むように定義された閉曲線．

閉ループ系の不安定極の数を知るために，右半面全体を覆う閉曲線に沿って $s$ を一周させる目的で定義される．  
基本的には
- 虚軸（ $j\omega$ 軸，$\omega = - \infty$ から $+ \infty$ ）と，
- 右半面を覆う半径無限大の半円  
から構成される．  

無限大半円状では，一巡伝達関数 $L(s)$ の値がほぼゼロに収束するため，結局は虚軸上の周波数応答（つまりベクトル軌跡）のみを考えればよいということになる．  
$L(s)$ が虚軸上に極や零点を持つ場合は，その点を避けるために虚軸上へ微小な半円状の迂回（インデンテーション）を挿入する必要がある．  
この経路を $L(s)$ 平面へ写像したものがナイキスト線図である．  
臨界点 $-1$ の周回数から偏角の原理を用いて閉ループ安定性を判定することができる．