# GEN7 瞬き乱数自動化ツール (Poke-Controller Modified Extension)

ポケットモンスター サン・ムーン / ウルトラサン・ウルトラムーン(第7世代)向けの乱数調整を自動化する、Poke-Controller Modified Extension 用の自動化プログラムです。

| コマンド名 | 内容 | 対応バージョン |
|---|---|---|
| `Gen7_ID_Adjust` | ID 調整 | SM / USUM |
| `Gen7_Gift_BlinkRNG` | ギフト個体の瞬き乱数調整 | US / UM |

`Gen7_Gift_BlinkRNG` の対象:

- ピカチュウ(サトシ)
- ベベノム(ウルトラメガロポリス)
- ベベノム(メガロタワー)
- タイプ:ヌル(エーテルパラダイス)

## 解説記事

詳しい使い方・設定方法は、以下の記事を参考にしてください。

- [【GEN7】3DS自動化-ID調整/ギフト系統瞬き乱数自動化-](https://note.com/deepindigo80/n/n98bae655e457)

## 動作環境

- [Poke-Controller Modified Extension](https://github.com/futo030/Poke-Controller-Modified-Extension)
  ```
- New Nintendo 3DS LL 本体
- 拡張コントローラー: <https://www.3dscontroller.com/>
- キャプチャボード: [3DS Capture](https://3dscapture.com)

## 導入方法

1. `numba` をインストールする(上記)
2. 本フォルダ一式を `Commands/PythonCommands/GEN7/` に配置する
3. Poke-Controller を起動し、コマンド一覧から `Gen7_ID_Adjust` または `Gen7_Gift_BlinkRNG` を選択して実行する

初回実行時は numba のコンパイルが入るため、計算開始まで少し時間がかかります(2回目以降はキャッシュされます)。

設定内容は `automations/settings/` に保存されます。

## ファイル構成

```
GEN7/
├─ automations/   # コマンド本体(ID調整 / ギフト個体瞬き乱数)
├─ core/          # 乱数計算(SFMT・瞬き・個体生成)、対象ごとの設定
├─ common/        # 画像判定・画面遷移・針読み取り・ウィジェット等の共通処理
└─ templates/     # テンプレートマッチ用画像
```

## ライセンス

[LICENSE](./LICENSE) を参照してください。概要は以下のとおりです。

- ✅ 個人での利用・自己利用のための改変: OK
- ✅ 本ツールを用いた乱数調整代行: OK
- ❌ 再配布(二次配布、改変版・派生物を含む): 禁止
- ❌ 商用利用(本ツールの販売、本ツールで入手したポケモンの販売など): 禁止
- 改変版・派生物を公開したい場合は、事前に作者へ連絡してください。
- 配布元へのリンクの紹介は自由です。

## 作者

RN ([@deepindigo80](https://x.com/deepindigo80))

## 謝辞

- 乱数計算のロジックは [3DS RNG Tool](https://github.com/wwwwwwzx/3DSRNGTool) を参考に Python へ移植しています。
- 本ツールは、[フウ様(@dragonite303)](https://x.com/dragonite303) が開発された [Poke-Controller Modified Extension](https://github.com/futo030/Poke-Controller-Modified-Extension) 上で動作します。
- 3DS の操作には、[らだま様(@lime_gree)](https://x.com/lime_gree) が開発された [3DS Controller](https://www.3dscontroller.com/) を使用しています。
