---
time: 2026-07-12T15:42
jp: 同一次元オブザーバ
en: Full-Order Observer
aliases:
  - 同一次元オブザーバ
  - 全次元オブザーバ
  - Full-Order State Observer
  - Full-State Observer
  - ルエンバーガーオブザーバ
tags:
  - 分野/制御工学/現代制御
  - 要素/手法・アルゴリズム
up:
  - "[[_Word/observer|オブザーバ]]"
sibling:
  - "[[_Word/minimal-order-observer|最小次元オブザーバ]]"
  - "[[_Word/kalman-filter|カルマンフィルタ]]"
pair:
  - "[[_Word/minimal-order-observer|最小次元オブザーバ]]"
person:
  - "[[_Name/david-luenberger|デイヴィッド・ルエンバーガー]]"
source:
  - https://digitalservo.jp/library/linear-control-design/observer-design/full-order-observer/
---
# 同一次元オブザーバ（Full-Order Observer）
> 制御対象の状態空間表現と同じ次数を持ち，全状態変数を推定するオブザーバ．

同一次元オブザーバは，制御対象の状態 $x$ の次元の数 $n$ と同じ次元をもつ．  
同一次元オブザーバの状態は $\hat{x}$ で表す．  

同一次元オブザーバの内部に，制御対象と同一の状態空間モデル（A, B, C行列）を構築し，同じ入力 $u$ を加えて，推定出力 $\hat{y}$ を生成する．  

実測出力 $y$ と，推定出力 $\hat{y}$ の差（=推定誤差）にオブザーバゲイン行列 $L$ を乗じ，状態の微分方程式に加算することで，推定状態を真の状態に収束させる．  

## 推定誤差のダイナミクス
推定誤差のダイナミクスは $A - LC$ の固有値で決まる．  
$(C, A)$ が可観測であれば，$L$ を適切に設計することで，推定誤差を任意の速さで収束させることができる．

## 状態FBゲインとオブザーバゲイン
状態FBゲイン $K$ とオブザーバゲイン $L$ は互いに独立に設計できる．  
両者を組み合わせた閉ループ系の極は，  
- 状態FB系の極　と
- オブザーバの極　との和集合になる．  ←分離定理