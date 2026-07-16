---
time: 2026-07-16T15:37
jp: 相互相関関数
en: Cross Correlation Function
aliases:
  - 相互相関関数
  - クロス相関関数
tags:
  - 分野/信号処理
  - 分野/数学/解析学
  - 要素/概念
  - 要素/モデル・数式
up:
  - "[[_Word/correlation-function|相関関数]]"
sibling:
  - "[[_Word/autocorrelation-function|自己相関関数]]"
pair:
  - "[[_Word/cross-spectral-density|クロススペクトル密度]]"
person:
  - "[[_Name/norbert-wiener|ノーバート・ウィーナー]]"
source:
  - https://ja.wikipedia.org/wiki/%E7%9B%B8%E4%BA%92%E7%9B%B8%E9%96%A2%E9%96%A2%E6%95%B0
---
# 相互相関関数（Cross Correlation Function）
> 2つの信号または時系列データの類似性を，時間差（ラグ）の関数として表したもの．

2つの信号 $x(t)$ と $y(t)$ について，一方を $\tau$ だけ時間シフトさせながら両者の席を積分することで得られる関数．  

2信号が完全に一致する場合に最大値（正規化すれば $1$ ）をとり，  
無相関の場合は $0$ に近づく．  

同一信号同士の場合，相互相関は自己相関関数と呼ばれ区別される．

## 用途
- 信号間の時間遅れの推定
- 外部雑音に埋もれた信号の検出
- 系の入出力関係の解析
