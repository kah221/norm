---
time: 2026-06-26T02:27
jp: ベクトル軌跡
en: Vector Locus
aliases:
  - ベクトル軌跡
tags:
  - 分野/制御工学/古典制御
  - 要素/手法・アルゴリズム
up:
  - "[[_Word/frequency-response-analysis|周波数応答解析]]"
sibling:
  - "[[_Word/bode-plot|ボード線図]]"
  - "[[_Word/nichols-plot|ニコルス線図]]"
  - "[[_Word/root-locus-method|根軌跡法]]"
pair:
person:
  - "[[_Name/harry-nyquist|ハリー・ナイキスト]]"
source:
  - https://controlabo.com/vector-locus/
---
# ベクトル軌跡（Vector Locus）
> 伝達関数の周波数伝達関数 $G(jω)$ を複素平面上にプロットし，$ω$ を $0$ から $∞$ まで変化させたときの軌跡．ゲインは原点からの距離，位相はベクトルの角度として表現される．

伝達関数 $G(s)$ の $s$ を $jω$ に置き換えた周波数伝達関数 $G(jω)$ は複素数であり，その実部・虚部をそれぞれ横軸・縦軸にとった複素平面（s-平面，ガウス平面）上の点として表現できる．  

利点  
：ボード線図はゲイン線図と位相線図の2つを見なければならないが，ベクトル軌跡では，1つの図だけでゲインと位相の両情報を表現できる．  

短所  
：周波数軸が無いため，どの点が度の周波数に対応するかは別途 $\omega$ の値を書き込む必要がある．