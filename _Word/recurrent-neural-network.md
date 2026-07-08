---
time: 2026-07-08T10:25
jp: リカレントニューラルネットワーク
en: Recurrent Neural Network
aliases:
  - リカレントニューラルネットワーク
  - RNN
  - 回帰型ニューラルネットワーク
  - 再帰型ニューラルネットワーク
tags:
  - 分野/情報工学
  - 要素/モデル・数式
up:
  - "[[_Word/neural-network|ニューラルネットワーク]]"
sibling:
  - "[[_Word/long-short-term-memory|LSTM]]"
  - "[[_Word/convolutional-neural-network|畳み込みニューラルネットワーク]]"
  - "[[_Word/transformer|Transformer]]"
pair:
  - "[[_Word/feedforward-neural-network|フィードフォワードニューラルネットワーク]]"
person:
  - "[[_Name/john-hopfield|ジョン・ホップフィールド]]"
  - "[[_Name/sepp-hochreiter|ゼップ・ホッホライター]]"
source:
  - https://aws.amazon.com/jp/what-is/recurrent-neural-network/
---
# リカレントニューラルネットワーク（Recurrent Neural Network, RNN）
> 隠れ層の出力を再び同じ隠れ層に戻す循環構造（再帰結合）を持ち，時系列データや系列データを処理できるニューラルネットワーク．

通常のフィードフォワードニューラルネットワーク（入力→隠れ層→出力 の一方向）と異なり，RNNは隠れ層の出力を次の時刻の隠れ層への入力として戻す循環構造を持つ．  
これにより過去の入力情報を記憶として保持し，文脈や時間的な依存関係を学習できる．  
近年は，「Transformerアーキテクチャ」に多くのタスクで置き換えられつつある．  
## 弱点
- 時系列が長くなると「勾配」が消失or爆発する
	- ↑遠い過去の情報を学習できなくなる
## 弱点の対応策
- LSTM（Long Short-Term Memory）
	- 忘却ゲート，入力ゲート，出力ゲートの2ゲート構造で，長期記憶を選択的に保持する
- GRU（Gated Recurrent Unit）
	- RNNの構造を簡略化したもの
## 応用例
- 自然言語処理
- 音声認識
- 機械翻訳
- 株価予測
- 動画解析
