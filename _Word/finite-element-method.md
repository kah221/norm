---
time: 2026-07-12T16:11
jp: 有限要素法
en: Finite Element Method
aliases:
  - "有限要素法"
  - "FEM"
  - "FEM解析"
  - "有限要素解析"
  - "FEA"
  - "Finite Element Analysis"
tags:
  - 分野/数学
  - 分野/機械力学
  - 要素/手法・アルゴリズム
up:
  - "[[_Word/numerical-analysis|数値解析]]"
sibling:
  - "[[_Word/finite-difference-method|差分法]]"
  - "[[_Word/boundary-element-method|境界要素法]]"
pair:
person:
  - "[[_Name/ray-clough|レイ・クラフ]]"
  - "[[_Name/olgierd-zienkiewicz|オルギエルト・ジェンキェヴィッチ]]"
source:
  - "https://ja.wikipedia.org/wiki/有限要素法"
---
# 有限要素法（Finite Element Method, FEM）
> 解析的に解くことが困難な偏微分方程式に対し，定義域を多数の小領域（要素）に分割し，各要素内で単純な補間関数による近似を行うことで数値的な近似解を得る手法．

解析対象の領域を，三角形・四面体などの小領域（要素）に分割し，各要素内の道関数を1次や2次の線形関数の多項式で近似する．  
元の偏微分方程式を積分形式の弱形式に変換し，各要素の要諦式を組み立てて全体の連立方程式を解くことで，各節点における変位・温度・電位などの近似値を得る．  

差分法と比べて，複雑な形状・境界条件への適応力が高い．  

## 解析の流れ
1. CADによる形状モデリング
2. メッシング（小領域に分割）
3. 境界条件・荷重の設定
4. 求解
5. 結果の可視化
## ソフトウェア
- Ansys（汎用FEMソフト） 
- Abaqus（非線形解析に強い，自動車，航空宇宙産業で底板）
- NASTRAN（NASAが1960年代に開発）
- COMSOL Multiphysics（複数の物理現象の連星解析に特化，音響・電磁場・化学反応などにも）
	- Acoustics Module：蝸牛内部の音波伝播シミュレーションも行われている
- Fusion360（簡易的なFEM解析ができる）