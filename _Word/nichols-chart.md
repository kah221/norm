---
time: 2026-11-05T00:54
jp: ニコルス線図
en: Nichols Chart
aliases:
  - ニコルス線図
  - ニコルズ線図
  - ニコルズチャート
  - Nichols Plot
  - Nichols Diagram
  - ゲイン位相線図
tags:
  - 分野/制御工学/古典制御
  - 要素/手法・アルゴリズム
up:
  - "[[_Word/frequency-response-analysis|周波数応答解析]]"
  - "[[magnitude-phase-plot|ゲイン位相線図]]"
sibling:
  - "[[_Word/bode-diagram|ボード線図]]"
  - "[[_Word/nyquist-diagram|ナイキスト線図]]"
  - "[[_Word/vector-locus|ベクトル軌跡]]"
  - "[[_Word/root-locus|根軌跡]]"
pair:
person:
  - "[[_Name/nathaniel-b-nichols|ナサニエル・B・ニコルス]]"
source:
  - https://ja.wikipedia.org/wiki/ニコルス線図
---
# ニコルス線図（Nichols Chart）
> ゲイン位相線図（縦軸 $|G(j\omega)|$ ，横軸 $\angle G(j\omega)$ ）上に，閉ループ伝達関数の大きさ $M$ が一定となる軌跡群（等M軌跡）を重ねた線図．

ニコルス線図は，等M軌跡を，ゲイン位相座標に移したものであり，ゲイン位相線図とは異なる．  

前提概念  
- ゲイン位相線図：周波数伝達関数の軌跡とその平面座標  
- 等M軌跡：ニコルス線図を構成する曲線軍  

<img src="../_A/ext/2026/11/202611_055639_nichols-chart.webp" alt="[外部著作物のため非公開]" width="400">
**Fig. 1**　ニコルス線図に軌跡を描いたもの
## 読み取れること
> ニコルス線図上に $G(j\omega)$ の軌跡を描くと，次の値が読み取れる．  

- 共振ピーク $M_r$ ： $G(j\omega)$ の軌跡に上側から接する等M軌跡のうち，最小のものの値．
- 共振周波数 $\omega_r$：その接点における $\omega$ 
- 帯域幅 $\mathrm{BW}$：$G(j\omega)$ の軌跡が $M = 0.707 \: (-3 \mathrm{dB})$ 軌跡と交わる点の周波数
- 閉ループのゲイン曲線 $|M(j\omega)|$ ：（等M軌跡と軌跡の各交点から）  

## ゲイン位相線図との違い
- ニコルス線図の上に，ゲイン位相線図（軌跡）を重ねて描くという使い方．
- 慣用的に，↑らを合わせてニコルス線図と呼ぶ場合もある．

|  Word   |                  Definition                  |
| :-----: | :------------------------------------------: |
| ゲイン位相線図 | 縦軸dB，横軸degの平面に，周波数伝達関数 $G(j\omega)$ の軌跡を描いた図 |
| ニコルス線図  |      縦軸dB，横軸degの平面に，等M軌跡の曲線軍を予め描いておいた図表      |
