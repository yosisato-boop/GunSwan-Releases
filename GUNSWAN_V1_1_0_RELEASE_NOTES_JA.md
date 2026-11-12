# GunSwan v1.1.0（Windows x64）

- 新Launcherはライブラリから通常起動、State復元、Session続行、ViewerとMovieキューを提供します。
- 割り込み可能なREPを含む製品既定CPUタイミングへ更新し、検証したFF戦闘BGMの進行を回復しました。
- PersistenceとAPUの処理を改善し、State・記録・巻き戻しで保持する実行状態を拡張しました。
- ViewerはBOOT中の音声も捕捉します。Movieは代替起動試行の失敗と実再生エラーを区別します。
- Windows x64の従来7本が対象です。
- LauncherのロゴとWindows実行ファイルのアイコンを更新しました。Owned censusではSTART入力に応答する静止タイトル画面を描画停止と区別します。
- Windows Launcherの既定の設定保存先を共通化しました。別フォルダーに展開した新しいバージョンでも同じ設定を読み込みます。
- LauncherのMovie作成後、出力先に作成した一時フォルダーを削除します。
- Launcherの保存先指定を共通設定に保存し、別のフォルダーに展開したバージョンでも同じライブラリ・Sessionを開きます。
- 同じROMの別機種Stateを開くと、保存時の機種に切り替えます。WSとWSCでは内蔵EEPROMのゲーム保存領域を共有できます。
- WonderSwan Color向けの動作確認サンプル「GunPuzzle for WSC - GunSwan Demo -」を同梱します。

## ダウンロード — Windows v1.1.0

**[Windows x64 ZIP](https://github.com/yosisato-boop/GunSwan-Releases/releases/download/v1.1.0/GunSwan-1.1.0-license-r1-windows-x64.zip)** / [SHA-256 ファイル](https://github.com/yosisato-boop/GunSwan-Releases/releases/download/v1.1.0/GunSwan-1.1.0-license-r1-windows-x64.zip.sha256) / [正式リリース](https://github.com/yosisato-boop/GunSwan-Releases/releases/tag/v1.1.0)

ZIP SHA-256: `28e52c0402cfff4913a5b376ba64d0f3b59e1100712ab75b014b1ced113c5d54`

動作確認サンプル「GunPuzzle for WSC - GunSwan Demo -」を同梱しています。更新時は新しいフォルダーにZIPを展開し、`gunswan-launcher.exe` を起動してください。保存先が共通設定に登録済みであれば、既存のライブラリとSessionを引き続き開けます。初めて引き継ぐ場合は、Launcherの設定で既存のユーザーデータフォルダーを指定してください。

[導入・操作](INSTALL.md)

## v1.1.0 既知の制限

- 旧Sessionは新しいCPUタイミングでStrict NonExactになる場合があります。原記録は保持してください。
- 旧Core v9と現行CoreのStateでは、同じ入力列での完全一致を保証しません。GSSTATE v2の読込可否は個々の互換判定に従います。
- 一部タイトルの表示差、CPU/PPU位相、ホスト依存の音声不足や終了時停止は検証範囲に制限があります。
- 別PC、全音声機器、外部BOOT、長時間Movieは未検証です。Movieには別途FFmpegが必要です。

Windows x64版です。GunSwan本体の利用条件はZIP内の LICENSE.txt、サンプルの条件とクレジットは samples フォルダーに記載しています。GitHubの自動生成 Source code アーカイブには公開案内文書が入ります。
