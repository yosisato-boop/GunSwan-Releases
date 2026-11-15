# GunSwan v1.1.1（Windows x64）

一部のWonderSwanカートリッジで、ROMフッターのSRAM宣言と実際の容量が異なり、ゲーム内セーブが正常に動作しない問題を修正しました。標準カートリッジの8 KiB宣言（`0x01`）を、共通のカートリッジ処理で実効32 KiBとして扱います。ROMの変更は不要です。STAR HEARTSでは、未改変ROMと復旧済み32 KiBセーブで「つづきから」の読み込みを確認しました。

Windowsでは、既存の8 KiB `.sav` の内容を先頭に保持して読み込み、初回の32 KiB保存前に元ファイルを `.sav.8k.bak` へ退避します。既に破損した内容は自動復旧しません。以前の8 KiB構成で記録したState・Sessionは、新しいSRAM構成と合わない場合に読み込みを拒否します。

同梱の動作確認サンプルはv1.1.0と同じ「GunPuzzle for WSC - GunSwan Demo -」です。その他の既知制限は同梱の known_limitations_ja.md をご覧ください。

[ダウンロード](https://github.com/yosisato-boop/GunSwan-Releases/releases/tag/v1.1.1) / [日本語LICENSE](GUNSWAN_V1_1_1_BINARY_LICENSE_JA.md) / [ビルド出自](GUNSWAN_V1_1_1_BUILD_PROVENANCE.json)
