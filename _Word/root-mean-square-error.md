---
time: 2026-10-20T01:32
jp: 二乗平均平方根誤差
en: Root Mean Square Error
aliases:
  - "二乗平均平方根誤差"
  - "RMSE"
  - "RMSD"
  - "平均平方根誤差"
  - "平方根平均二乗誤差"
  - "Root Mean Square Deviation"
  - "Root Mean Squared Error"
tags:
  - 分野/数学
  - 分野/情報工学
  - 要素/指標
up:
  - "[[_Word/regression-evaluation-metric|回帰評価指標]]"
sibling:
  - "[[_Word/mean-squared-error|平均二乗誤差]]"
  - "[[_Word/mean-absolute-error|平均絶対誤差]]"
  - "[[_Word/coefficient-of-determination|決定係数]]"
pair:
person:
source:
  - "https://ja.wikipedia.org/wiki/二乗平均平方根誤差"
---
# 二乗平均平方根誤差（Root Mean Square Error, RMSE）
> 予測値（推定値）と観測値の差を二乗して平均し，その平方根をとった誤差の尺度．

n個のデータについて，観測値を $y_i$ ，予測値を $\hat{y}_i$ とすると，RMSEは次式で定義される．

$$
\mathrm{RMSE} = \sqrt{\frac{1}{n} \Sigma (\hat{y}_1 - y_i)^2}
$$
平均二乗誤差 MSE の平方根にあたる．平方根を取ることで，元のデータと同一の単位となる．  
誤差を二乗してから平均するため，大きな誤差ほど影響が大きくなり，外れ値に敏感になる．  

★  
- 外れ値を重視したくない場合 → 平均絶対誤差 MAE が良い  
- 大きな予測ミスを許容できない場合 → RMSE が良い
