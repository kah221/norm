---
time: 2026-07-13T23:46
jp: 位相余裕
en: Phase Margin
aliases:
  - 位相余裕
  - PM
tags:
  - 分野/制御工学/古典制御
  - 要素/指標
up:
  - "[[_Word/stability-margin|安定余裕]]"
sibling:
  - "[[_Word/gain-margin|ゲイン余裕]]"
pair:
  - "[[_Word/gain-margin|ゲイン余裕]]"
person:
  - "[[_Name/hendrik-bode|ヘンドリック・ボーデ]]"
source:
  - https://controlabo.com/stability-margin/
---
# 位相余裕（Phase Margin, PM）
> 開ループ伝達関数のゲインが $0 \: \mathrm{dB}$ となるゲイン交差周波数 $\omega_P$ において，位相が $- 180 \: \mathrm{deg}$ からどれだけ余裕があるかを表す安定度指標．

## 性質
- 位相余裕の大きさは，システムがどの程度の位相遅れ迄安定性を保てるか？を示す．
- 位相余裕が正：閉ループ安定
- 位相余裕が0：[臨界安定](_Word/marginal-stability.md)
- 位相余裕が負：不安定
## 推奨値
- サーボ系：40 ~ 65度
- プロセス制御：15 ~ 70度  

## 位相余裕改善手法
- 位相進み要素など

## 読み取り
### ボード線図上では，
位相余裕 $\phi_M$ は，ゲイン線図が $0 \: \mathrm{dB}$ を横切る周波数 $\omega_P$ を読み取り，その周波数での位相線図の値と $-180 \: \mathrm{deg}$ の差  
### ナイキスト線図上では，
位相余裕 $\phi_M$ は，ベクトル軌跡が単位円と交わる点での偏角と，$-180 \: \mathrm{deg}$ の差  