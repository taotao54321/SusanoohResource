+++
title = "アイテム"
date = 2022-12-10
updated = 2022-12-23
+++

通常プレイで出現しないものも含む。

命中補正は近接武器にのみ存在する。  
遠隔武器にも命中補正と思しきデータはあるが、[遠隔武器の命中率計算](@/battle-damage/index.md#damage-rank-normal)では誤って近接命中補正を参照しており、結果として補正値が一律 0 になっている。

売値は基本的には買値の 1/4 だが、一部例外がある(買値は店ごと、売値はアイテムごとに設定されているため)。

| ID  | 名前             | 装備     | 道具 | 売却 | 攻撃 | 命中 | 防御 | 買値        | 売値 | 備考                                             |
| --: | --               | :-:      | :-:  | :-:  | --:  | --:  | --:  | --:         | --:  | --                                               |
| 0   | しょくりょう     |          | o    | o    |      |      |      | 0           | 0    |                                                  |
| 1   | てなげだん       |          | o    | o    |      |      |      | 45          | 3    |                                                  |
| 2   | くすり           |          | o    | o    |      |      |      | 10          | 2    |                                                  |
| 3   | しろがねの兜     | 兜       |      |      |      |      | 20   | 0           | 0    |                                                  |
| 4   | かがみの盾       | 盾       | o    |      |      |      | 80   | 0           | 0    | 特殊効果ID: 93                                   |
| 5   | 退魔の鎧         | 鎧       |      |      |      |      | 120  | 0           | 0    |                                                  |
| 6   | クサナギの剣     | 近接武器 | o    |      | 255  | 32   |      | 0           | 0    | 特殊効果ID: 236                                  |
| 7   | マガタマ         |          | o    |      |      |      |      | 0           | 0    | 特殊効果ID: 237                                  |
| 8   | ゆめの兜         | 兜       |      |      |      |      | 32   | 0           | 0    |                                                  |
| 9   | 力の鎧           | 鎧       |      |      |      |      | 55   | 0           | 0    |                                                  |
| 10  | 力の盾           | 盾       |      |      |      |      | 32   | 0           | 0    |                                                  |
| 11  | 力の剣           | 近接武器 |      |      | 255  | 32   |      | 0           | 0    |                                                  |
| 12  | ひかりのころも   | 鎧       |      |      |      |      | 255  | 0           | 0    |                                                  |
| 13  | あんしスコープ   |          | o    |      |      |      |      | 0           | 0    |                                                  |
| 14  | レコーダ         |          | o    |      |      |      |      | 3500        | 875  |                                                  |
| 15  | テープ           |          | o    |      |      |      |      | 0           | 0    |                                                  |
| 16  | PKばくだん       |          | o    | o    |      |      |      | 0           | 0    | 特殊効果ID: 129                                  |
| 17  | Eカプセル        |          | o    |      |      |      |      | 0           | 0    |                                                  |
| 18  | ひいずるかがみ   |          | o    |      |      |      |      | 0           | 0    |                                                  |
| 19  | はねばしのカギ   |          | o    | o    |      |      |      | 0           | 0    | 特殊効果ID: 86                                   |
| 20  | みずのほうせき   |          | o    |      |      |      |      | 0           | 0    |                                                  |
| 21  | ほのおのほうせき |          | o    |      |      |      |      | 0           | 0    | 特殊効果ID: 158                                  |
| 22  | ガソリン         |          | o    |      |      |      |      | 170         | 42   |                                                  |
| 23  | ほぞんしょく     |          | o    |      |      |      |      | 0           | 0    |                                                  |
| 24  | さいみんガス     |          |      | o    |      |      |      | 0           | 0    |                                                  |
| 25  | どくガス         |          | o    | o    |      |      |      | 0           | 0    |                                                  |
| 26  | さんそタンク     |          | o    | o    |      |      |      | 1500        | 375  | 特殊効果ID: 193                                  |
| 27  | シュノーケル     |          | o    | o    |      |      |      | 200         | 50   | 特殊効果ID: 195                                  |
| 28  | ガスマスク       |          | o    | o    |      |      |      | 0           | 0    |                                                  |
| 29  | ボウガン         | 遠隔武器 |      | o    | 18   |      |      | 50          | 12   |                                                  |
| 30  | きのボウガン     | 遠隔武器 |      | o    | 23   |      |      | 120         | 20   |                                                  |
| 31  | てつのボウガン   | 遠隔武器 |      | o    | 29   |      |      | 250         | 62   |                                                  |
| 32  | ロケットボウガン | 遠隔武器 |      | o    | 39   |      |      | 450         | 112  |                                                  |
| 33  | ジャベリン       | 遠隔武器 |      | o    | 33   |      |      | 0           | 0    |                                                  |
| 34  | ピストル         | 遠隔武器 |      | o    | 49   |      |      | 800         | 200  |                                                  |
| 35  | Sマシンガン      | 遠隔武器 |      | o    | 64   |      |      | 1200        | 300  |                                                  |
| 36  | マシンガン       | 遠隔武器 |      | o    | 83   |      |      | 1640        | 410  |                                                  |
| 37  | Aライフル        | 遠隔武器 |      | o    | 95   |      |      | 2200        | 550  |                                                  |
| 38  | ロケットランチャ | 遠隔武器 |      | o    | 190  |      |      | 5500        | 1375 |                                                  |
| 39  | かえんほうしゃき | 遠隔武器 |      | o    | 140  |      |      | 3000        | 750  |                                                  |
| 40  | ぼうきれ         | 近接武器 |      | o    | 3    | 5    |      | 4           | 1    |                                                  |
| 41  | ナイフ           | 近接武器 |      | o    | 9    | 9    |      | 40          | 10   |                                                  |
| 42  | スチールパイプ   | 近接武器 |      | o    | 35   | 6    |      | 250         | 62   |                                                  |
| 43  | サバイバルナイフ | 近接武器 |      | o    | 22   | 12   |      | 190         | 47   |                                                  |
| 44  | メイス           | 近接武器 |      | o    | 40   | 0    |      | 400         | 100  |                                                  |
| 45  | にほんとう       | 近接武器 |      | o    | 60   | 11   |      | 950         | 237  |                                                  |
| 46  | カトラス         | 近接武器 |      | o    | 58   | 20   |      | 950         | 237  |                                                  |
| 47  | おの             | 近接武器 |      | o    | 69   | 0    |      | 1300        | 325  |                                                  |
| 48  | ざんばとう       | 近接武器 |      | o    | 100  | 3    |      | 1500        | 375  |                                                  |
| 49  | レーザーナイフ   | 近接武器 |      | o    | 120  | 20   |      | 1700        | 425  |                                                  |
| 50  | ぼうし           | 兜       |      | o    |      |      | 4    | 30          | 7    |                                                  |
| 51  | ヘルメット       | 兜       |      | o    |      |      | 9    | 100         | 25   |                                                  |
| 52  | てつかぶと       | 兜       |      | o    |      |      | 13   | 160         | 30   |                                                  |
| 53  | のうはヘルメット | 兜       |      | o    |      |      | 17   | 1500        | 375  |                                                  |
| 54  | ふく             | 鎧       |      | o    |      |      | 5    | 50          | 12   |                                                  |
| 55  | かわの鎧         | 鎧       |      | o    |      |      | 7    | 160         | 40   |                                                  |
| 56  | ぼうだんチョッキ | 鎧       |      | o    |      |      | 15   | 250         | 62   |                                                  |
| 57  | アーマー         | 鎧       |      | o    |      |      | 25   | 850         | 212  |                                                  |
| 58  | セラミックスーツ | 鎧       |      | o    |      |      | 40   | 1200 (1000) | 250  | 山の村西では買値 1200, ぎじゅつの町では買値 1000 |
| 59  | きの盾           | 盾       |      | o    |      |      | 5    | 70          | 17   |                                                  |
| 60  | てつの盾         | 盾       |      | o    |      |      | 10   | 180         | 40   |                                                  |
| 61  | とうめいの盾     | 盾       |      | o    |      |      | 19   | 200         | 50   |                                                  |
| 62  | ごうきんZの盾    | 盾       |      | o    |      |      | 24   | 400         | 100  |                                                  |
| 63  | ニューZの盾      | 盾       |      | o    |      |      | 30   | 950         | 150  |                                                  |
| 64  | アーマードスーツ | 全身     |      | o    | 210  |      | 120  | 30000       | 7500 |                                                  |
| 65  | パスワード       |          | o    |      |      |      |      | 0           | 0    | 特殊効果ID: 168                                  |
| 66  | ふうじのたま     |          | o    |      |      |      |      | 0           | 0    |                                                  |
| 67  | みずきり         |          | o    |      |      |      |      | 0           | 0    |                                                  |
| 68  | かいほうのカギ   |          | o    |      |      |      |      | 0           | 0    | 特殊効果ID: 116                                  |
| 69  | はしらのカギ     |          | o    |      |      |      |      | 0           | 0    | 特殊効果ID: 144                                  |
| 70  | IDカード         |          | o    |      |      |      |      | 0           | 0    |                                                  |
| 71  | てがみ           |          | o    |      |      |      |      | 0           | 0    | 特殊効果ID: 80                                   |
| 72  | ほしゅうパーツ   |          | o    |      |      |      |      | 0           | 0    |                                                  |
| 73  | 魔のロウソク     |          | o    |      |      |      |      | 0           | 0    | 特殊効果ID: 48                                   |
| 74  | アルミの盾       | 盾       |      | o    |      |      | 7    | 140         | 35   |                                                  |
| 75  | ささやきのいし   |          | o    |      |      |      |      | 0           | 0    |                                                  |
| 76  | ポリタンク       |          | o    | o    |      |      |      | 0           | 0    |                                                  |
| 77  | げんゆ           |          | o    | o    |      |      |      | 0           | 0    |                                                  |
| 78  | 村長のてがみ     |          | o    |      |      |      |      | 0           | 0    |                                                  |
| 79  | かいふくやく     |          | o    | o    |      |      |      | 0           | 0    | 特殊効果ID: 190                                  |
| 80  | バリアマシン     |          | o    | o    |      |      |      | 4500        | 1250 | 特殊効果ID: 191                                  |
| 81  | ハイパーバリア   |          | o    | o    |      |      |      | 15000       | 3750 | 特殊効果ID: 192                                  |
| 82  | ペンダント       |          | o    |      |      |      |      | 0           | 0    |                                                  |
| 83  | HUカード         |          | o    | o    |      |      |      | 1           | 0    |                                                  |
