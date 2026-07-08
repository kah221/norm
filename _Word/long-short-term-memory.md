---
time: 2026-07-08T10:34
jp: LSTM
en: Long Short-Term Memory
aliases:
  - LSTM
  - 長・短期記憶
  - 長短期記憶
tags:
  - 分野/情報工学
  - 要素/モデル・数式
up:
  - "[[_Word/recurrent-neural-network|リカレントニューラルネットワーク]]"
sibling:
  - "[[_Word/gated-recurrent-unit|GRU]]"
  - "[[_Word/transformer|Transformer]]"
pair:
person:
  - "[[_Name/sepp-hochreiter|ゼップ・ホッホライター]]"
  - "[[_Name/juergen-schmidhuber|ユルゲン・シュミットフーバー]]"
source:
  - https://cvml-expertguide.net/terms/dl/rnn/lstm/
---
# LSTM（Long Short-Term Memory, LSTM）
> RNNの勾配消失問題を解決するために，記憶セルとゲート機構を導入し，長期の時系列依存関係を学習できるようにした改良版RNNアーキテクチャ．

1997年に提案され，2000年に忘却ゲートが追加され広く普及した．  
通常のRNNの遠い過去の情報を学習できない問題を解決する手法．  
構造を簡略化した派生としてGRUがある．  
## 構成要素
- 「セル状態 $C_t$ ：長期記憶を運ぶコンベアベルト」を導入し，セル状態の更新を乗算的ではなく，加法的に行う．  
	- →勾配が減衰なく伝播する経路（CEC：Constant Error Carousel）を確保．
- 3つのゲートでセル状態への情報の出し入れを制御
	- 忘却ゲート $f_t$ ：過去の記憶のうち何を捨てるか
	- 入力ゲート $i_t$ ：新しい情報のうち何を記憶するか
	- 出力ゲート $o_t$ ：記憶のうち何を出力するか
- 各ゲートはシグモイド関数で0, 1の値を取り，データに応じて開閉度合いが学習される．