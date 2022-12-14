+++
title = "RAM マップ"
date = 2022-12-24
+++

## 概要

| アドレス | 型 | 内容 |
| --       | -- | --   |
|`$2018`|`u8`|`$0000` へ書き込んだ値を保持する(VDC 操作中に割り込まれても壊れないようにするため)|
|`$2019`|`u8`|VDC 制御レジスタ管理用|
|`$204D`|`ptr`|(ビット列処理ルーチン用) ビット列を格納したバッファへのポインタ|
|`$204F`|`u8`|(ビット列処理ルーチン用) 現在のビット位置(値は2冪)|
|`$2050`|`u8`|(ビット列処理ルーチン用) 初期ビット位置(値は2冪)|
|`$2200`|`u8`|常に 0|
|`$2209-$220D`|`u8[5]`|1P から 5P までの生[入力](#input)|
|`$220E-$2212`|`u8[5]`|1P から 5P までのエッジ[入力](#input)|
|`$2213`|`u8`|先行[入力](#input)バッファ。1Pエッジ入力が OR される|
|`$2216`|`u8`|VSYNC 割り込みが有効か (0:false, 1:true)|
|`$2217`|`u8`|VSYNC カウンタ|
|`$2218`|`u8`|常に 0|
|`$2219`|`u16le`|[乱数生成器](@/rng/index.md)の内部状態|
|`$2261`|`i16le`|現在のマップ内座標x|
|`$2263`|`i16le`|現在のマップ内座標y|
|`$2265`|`u8`|現在のマップID|
|`$2276`|`u8`|現在のウィンドウ階層|
|`$2280`|`u16le`|所持金|
|`$2282`|`u16le`|経験値|
|`$2284`|`u8`|食料所持数|
|`$2285`|`u8`|手投げ弾所持数|
|`$2286`|`u8`|薬所持数|
|`$2287-$229C`|`u8`|インベントリ (0xFF 終端)。便宜上、`$2284-$229C` をインベントリとして扱うこともある|
|`$229D-$229F`|`u8[3]`|各PTキャラのキャラID (0xFF で不在)|
|`$22A0-$22A2`|`u8[3]`|各PTキャラの装備武器 (値はインベントリ内インデックス。0xFF で無装備)|
|`$22A3-$22A5`|`u8[3]`|各PTキャラの装備兜 (値はインベントリ内インデックス。0xFF で無装備)|
|`$22A6-$22A8`|`u8[3]`|各PTキャラの装備鎧 (値はインベントリ内インデックス。0xFF で無装備)|
|`$22A9-$22AB`|`u8[3]`|各PTキャラの装備盾 (値はインベントリ内インデックス。0xFF で無装備)|
|`$22AC-$22AE`|`u8[3]`|各PTキャラのブロックされているESP (bit0:テレポート, bit1:レビ, bit2:ホールド, bit3:キュア, bit4:バリア, bit5:フレア, bit6:ウェーブ, bit7:PK)|
|`$22AF`|`u8`|現在乗っている[乗り物](#transporter)|
|`$22B2-$22C9`|`u8[24]`|各戦闘キャラの所属陣営 (0:なし, 1:味方, 2:敵)|
|`$22CA-$22E1`|`u8[24]`|各戦闘キャラのID (味方ならキャラID, 敵なら敵ID)|
|`$22E2-$22F9`|`u8[24]`|各戦闘キャラの座標x|
|`$2312-$2329`|`u8[24]`|各戦闘キャラの座標y|
|`$23D2-$23E9`|`u8[24]`|各戦闘キャラの現在HP|
|`$23EA-$2401`|`u8[24]`|各戦闘キャラの最大HP|
|`$2402-$2419`|`u8[24]`|各戦闘キャラの現在MP|
|`$241A-$2431`|`u8[24]`|各戦闘キャラの最大MP|
|`$2432-$2449`|`u8[24]`|各戦闘キャラのOP|
|`$244A-$2461`|`u8[24]`|各戦闘キャラのSTR|
|`$2462-$2479`|`u8[24]`|各戦闘キャラのMDX|
|`$247A-$2491`|`u8[24]`|各戦闘キャラのDEX|
|`$2492-$24A9`|`u8[24]`|各戦闘キャラのVIT|
|`$24AA-$24C1`|`u8[24]`|各戦闘キャラの内部LV|
|`$24F2-$2509`|`u8[24]`|各戦闘キャラのバリアレベル|
|`$2523`|`u8`|現在見ているアイテムの各種フラグ (bit0:近接武器, bit1:遠隔武器, bit2:鎧, bit3:盾, bit4:兜, bit5:道具欄に現れる, bit6:売却不可, bit7:道具使用時にイベントスクリプトを実行)|
|`$2524`|`u8`|現在見ているアイテムの近接攻撃力|
|`$2525`|`u8`|現在見ているアイテムの遠隔攻撃力|
|`$2526`|`u8`|現在見ているアイテムの遠隔武器プロパティ Byte2 (write-only?)|
|`$2527`|`u8`|現在見ているアイテムの近接命中補正|
|`$2528`|`u8`|現在見ているアイテムの遠隔武器プロパティ Byte1 (write-only?)|
|`$2529`|`u8`|現在見ているアイテムの防御力|
|`$252A`|`u8`|現在見ているアイテムの防具プロパティ Byte1 (write-only?)|
|`$252B`|`u8`|現在見ているアイテムのイベントスクリプトID|
|`$26F9`|`u8`|戦闘: 現在のダメージ攻撃のダメージランク (0:E, 1:A, 2:B, 3:C, 4:D)|
|`$26FB`|`u8`|ストーリー進行度|
|`$2770`|`u8`|HP表示設定 (0:左, 1:右, 2:なし)|
|`$2776`|`u8`|現在見ているキャラの習得ESPレベル: PK|
|`$2777`|`u8`|現在見ているキャラの習得ESPレベル: ウェーブ|
|`$2778`|`u8`|現在見ているキャラの習得ESPレベル: フレア|
|`$2779`|`u8`|現在見ているキャラの習得ESPレベル: バリア|
|`$277A`|`u8`|現在見ているキャラの習得ESPレベル: キュア|
|`$277B`|`u8`|現在見ているキャラの習得ESPレベル: ホールド|
|`$277C`|`u8`|現在見ているキャラの習得ESPレベル: レビ|
|`$277D`|`u8`|現在見ているキャラの習得ESPレベル: テレポート|
|`$277F`|`u8`|使用するESP (bit0-1:レベル(0-based), bit2-4:種類(0:PK,1:ウェーブ,2:フレア,3:バリア,4:キュア,5:ホールド,6:レビ,7:テレポート))|
|`$2781`|`u8`|時刻 (0:朝, 1:昼, 2:夕方, 3:夜)。bit7 は闇の大陸フラグ|
|`$2782`|`u8`|時刻タイマー (`0..=15`)|
|`$2783`|`u8`|メッセージ速度 (0-based)|
|`$2784`|`u8`|バトルメッセージ表示設定 (0:表示, 1:非表示)|
|`$2785`|`u8`|待機中の[乗り物](#transporter)|
|`$2786`|`i16le`|待機中の乗り物のマップ内座標x|
|`$2788`|`i16le`|待機中の乗り物のマップ内座標y|
|`$279E`|`u8`|MPR 退避用スタックポインタ|
|`$279F-`||MPR 退避用スタック|
|`$281A`|`u8`|戦闘: 現在のダメージ攻撃の種類 (0:遠隔, 1:近接, 2:ESP, 3:手投げ弾)|
|`$2C95`|`u8`|戦闘: 次の 1 歩がOP内での第 1 歩であるか (0:false, 1:true)。false のとき、さらに歩くとOPを消費する|
|`$2C96`|`u8`|戦闘: ダメージ計算結果|
|`$2CB6`|`u8`|戦闘: ターゲットカーソル記憶用|
|`$2CBF`|`u8`|戦闘: 敵を倒した際の獲得経験値|
|`$2CC0`|`u8`|戦闘: 敵を倒した際の獲得金額|


## コントローラー入力 {#input}

| bit | キー   |
| --  | --     |
| 0   | I      |
| 1   | II     |
| 2   | Select |
| 3   | Run    |
| 4   | Up     |
| 5   | Right  |
| 6   | Down   |
| 7   | Left   |


## 乗り物 {#transporter}

| 値 | 種類           |
| -- | --             |
| 0  | (なし)         |
| 1  | タグボート     |
| 2  | 外洋船         |
| 3  | ホバークラフト |
| 4  | 飛行機         |
| 5  | ラングーン     |
