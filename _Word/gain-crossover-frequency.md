---
time: 2026-07-14T01:09
jp: ゲイン交差周波数
en: Gain Crossover Frequency
aliases:
  - "ゲイン交差周波数"
tags:
  - 分野/制御工学/古典制御
  - 要素/指標
up:
  - "[[_Word/bode-diagram|ボード線図]]"
sibling:
  - "[[_Word/phase-crossover-frequency|位相交差周波数]]"
pair:
  - "[[_Word/phase-crossover-frequency|位相交差周波数]]"
person:
  - "[[_Name/hendrik-bode|ヘンドリック・ボーデ]]"
source:
  - "https://controlabo.com/stability-margin/"
---
# ゲイン交差周波数（Gain Crossover Frequency, $\omega_{cg}$, $\omega_P$）
> 開ループ伝達関数のゲインが $0 \: \mathrm{dB} \:\: (=1)$ となる角周波数．

## 性質
- ゲイン交差周波数 $\omega_{cg}$ は，[位相余裕](_Word/phase-margin.md)を読み取る周波数
- FBループを一巡した信号の振幅が，ちょうど $1$ 倍になる周波数のこと
- これより低い周波数帯では，FBが有効に効く帯域（ゲインが1以上）
- これより高い周波数帯では，FBがほぼ効かない帯域（ゲインが1以下）
- ゲイン交差周波数は，おおよその制御帯域幅の目安
- ゲイン交差周波数が高いほど
	- 早い応答が得られるが，
	- 高周波域ででのモデル不確かさやノイズの影響を受けやすくなる
## 読み取り
### ボード線図
ゲイン線図において，ゲイン曲線が $0 \: \mathrm{dB}$ の水平線と交わる周波数
### ナイキスト線図
ベクトル軌跡と単位円との交点 $\mathrm{P}$ における周波数