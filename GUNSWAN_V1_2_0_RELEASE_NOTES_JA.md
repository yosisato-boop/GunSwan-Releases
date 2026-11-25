# GunSwan 1.2.0 — Windows x64

## v1.1.1からの主な変更

- IRETで再開したREP転送の途中で、次の割り込みを受理できるようにしました。Final Fantasyでは、会話ウィンドウのちらつきや戦闘BGMの途切れに関係する割り込み経路を修正しました。
- AAM／AADは命令の即値を使います。実機に基づき、DIV／IDIVと AAM 00 のINT0は次の命令のIPを保存します。
- WSC実機に合わせ、D6はALをFFhにし、AHとFLAGSを保持します。PUSHFと割り込み・例外がスタックに保存するPSWの固定・予約ビットを修正しました。
- タイマーI/O、割り込みベース（INT_BASE）、パレットI/Oの挙動を修正しました。
- 適格な旧Stateから継続できます。移行前のStateを保持し、新規Stateは現在の保存枠へ保存します。SRAM／EEPROM／RTCの永続データ形式は維持しています。
- Owned55の全55タイトルで本編到達・基本操作を回帰検証しました。対象は各タイトルの指定区間です。

## Windows v1.1.1 からの引き継ぎ

Launcherの対象ゲームで「このStateから開始」を選び、旧Stateを指定してください。本体起動時の `--load-state` も利用できます。移行に成功すると、新しいSessionで開始します。旧Stateは保持されます。保存時の割り込み状態を一意に復元できないStateは、読み込み時に理由を表示します。その場合は記録元の版で開いてください。ゲーム内のQuick Loadは現行モデルの保存枠を使用します。

| データ | 取り扱い |
|---|---|
| 移行可能な旧State | Stateから開始して新しいSessionで継続 |
| 対応する旧Session v3 | Best Effort。旧記録と異なる映像・音声・進行が生じる場合あり |
| 旧r1のGSXSESS・旧記録のStrict再生 | 記録元のビルドを使用 |
| v1.2.0で新規作成した記録 | 同じ時間モデルと対応する実行条件でStrict検証 |

**ROM横の `.sav`** は、保存デバイスとファイル容量が一致し、自動 `.sav` が有効なら通常起動で引き継げます。Launcherの「このStateから開始」や「続きから開始」では、State内のセーブ内容で再開し、正常終了時などにその時点の内容で共通 `.sav` を上書きします。古いStateから再開するとゲーム内のセーブもその時点に戻ります。旧8 KiB構成のState・Sessionは容量不一致で開けませんが、対象の旧8 KiB生 `.sav` は引き継げます。

同じROMの対応するStateは保存時の機種で再開します。WS・WSC・SwanCrystalの切替でCPUタイミングや保存容量の制約は解消されません。対象タイトルと詳細は 同梱の `known_limitations_ja.md` を参照してください。

## ダウンロードと確認

配布ZIPを新しいフォルダーに展開し、`gunswan-launcher.exe` を起動してください。ZIPのSHA-256は配布時の付属ファイル、展開内容は `SHA256SUMS.txt` と照合できます。利用条件は `LICENSE.txt`、ビルド元は `release-manifest.json` を参照してください。

[ダウンロード](https://github.com/yosisato-boop/GunSwan-Releases/releases/tag/v1.2.0) / [日本語LICENSE](GUNSWAN_V1_2_0_BINARY_LICENSE_JA.md) / [ビルド出自](GUNSWAN_V1_2_0_BUILD_PROVENANCE.json)
