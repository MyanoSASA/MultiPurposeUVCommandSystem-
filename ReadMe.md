# 概要
- ストワで動く遠隔操作な無人コンポーネントの色々をここに書く
- ロストテクノロジー的なのを掘り起こしているので詳しくは知りません。
# 通信規格メモ
## コンポジット通信内容(あくまで無人ヘリの内容。いろいろ不明)
### 機体→ターミナル
#### Number
- 11:ステータス（）
- 12:高度(無人ヘリでは対地高度)
- 13:機体側で記憶済みの目標X座標（？）
- 14:機体側で記憶済みの目標Y座標（？）
- 15:外部ユニット用汎用入力（無人ヘリではRadiation Detector）
#### Bool
- 11:ハードポイントのいずれかが接続済み
### ターミナル→機体
#### Number
- 1:目標X座標&目標着陸ビーコンの周波数
- 2:目標Y座標
- 12:カメラのFOV
#### Bool
- 1:離着陸命令
- 2:ウェイポイントまでの飛行命令
- 3:マニュアルコントロール(マニュアル操作時常時オンの必要あり)
- 4:カメラIR信号(オンの時IR)
