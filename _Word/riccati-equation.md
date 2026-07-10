---
time: 2026-07-10T09:38
jp: リカッチ方程式
en: Riccati Equation
aliases:
  - "リカッチ方程式"
  - "リッカチ方程式"
  - "Riccati方程式"
tags:
  - 分野/制御工学/現代制御
  - 分野/数学
  - 要素/モデル・数式
up:
  - "[[_Word/optimal-control|最適制御]]"
sibling:
  - "[[_Word/lyapunov-equation|リアプノフ方程式]]"
pair:
person:
  - "[[_Name/jacopo-riccati|ヤーコポ・リカッチ]]"
  - "[[_Name/rudolf-kalman|ルドルフ・カルマン]]"
  - "[[_Name/suguru-arimoto|有本 卓]]"
source:
  - "https://blog.control-theory.com/entry/lqr-state-feedback"
---
# リカッチ方程式（Riccati Equation）
> 未知変数の2次の非線形項を含む行列方程式で，最適制御やカルマンフィルタの設計において中心的な役割を果たす．

18世紀にヤーコポ・リカッチが研究したスカラーの1次乗微分方程式 $y' = a(x)y^2 + b(s)y + c(x)$ だが，  
制御工学ではこれを行列形式に拡張した2つの形が重要．  

- 微分リカッチ方程式（DRE）は，有限時間最適制御問題から導かれ，行列 $P(t)$ の時間発展を記述する．
- 終端時刻を無限大に飛ばすと，$P(t)$ は定常値に収束し，その定常解は時間微分項をゼロとおいたリカッチ代数方程式（ARE）を満たす．  