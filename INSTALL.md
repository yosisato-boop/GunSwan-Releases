GunSwan — developed by さっち / Copyright © 2026 さっち

# 導入・操作

導入・操作の説明です。

Windows x64、Microsoft Visual C++ v14 Redistributable x64が必要です。
Windows 11開発環境と別PCでの機能確認はありますが、v1.0.0の別PC確認のOS/Runtime詳細は未記録です。1.0.1の新しいClean Windows試験とは区別します。
最小Windows版や全driverでの動作は保証していません。
[Microsoft公式Runtime案内](https://learn.microsoft.com/en-us/cpp/windows/latest-supported-vc-redist?view=msvc-170)
からx64用を確認してください。不足DLLが出た場合はメッセージを記録します。
第三者のDLL単体配布サイトから取得しないでください。

1. [SHAを確認](DOWNLOAD.md)してZIPを展開します。
2. GunSwanフォルダー内のファイルを一緒に保持します。
3. gunswan-launcher.exeで自身の.ws/.wsc ROMを指定し、START GUNSWANを選びます。
4. LCD appearanceからRaw/WS/WSC/Crystalを選べます。LCD LabではCustomを調整できます。

矢印はX方向、WASDはY方向、ZはA、XはB、EnterはSTARTです。
P/SpaceはPause、NはPause中の1フレーム送り、F11はFullscreenです。
Inputメニューでキー・ゲームパッドを設定できます。Displayで倍率とDebug表示を変更します。

Stateメニューで保存/復元、F5でQuick Save、F8でQuick Load、slot0～9を選択できます。
Rewind有効時はゲームパッド両トリガーを保持して開きます。左右で選択、物理A(下)または
Escapeで取消、物理B(右)またはEnterで決定します。復元後の継続は旧未来を無効にします。
別の続きが必要なら、アプリを閉じてSessionを複製・バックアップしてください。

Session/State/設定の既定保存先は主に%LOCALAPPDATA%\GunSwan、補助は%APPDATA%\GunSwanです。
明示指定・ROM隣接保存設定によって異なります。関連Session一式を閉じてからバックアップします。
終了時の保存を待ち、保存先の権限と空き容量を確保してください。

OPEN SESSION VIEWERは既存SessionをREAD ONLYで再生し、原記録を書き換えません。
1/4x、1/2x、1x、高速再生とPause、LCD切替があります。

Movieは別途[FFmpeg公式案内](https://ffmpeg.org/download.html)から用意したffmpeg.exeを
Launcherで指定します。ROM・Keylog・MP4出力先・範囲・倍率・LCDを設定しCREATE MP4を選びます。
FFmpegなしでも通常プレイは可能です。FFmpeg/VC++ Runtimeを自動導入・同梱しません。
通常Movieの生成成功はStrictExact検証の合格を意味しません。

保存失敗・起動不能・音切れは、版、環境、操作、エラー全文をIssueで報告してください。
ROM/BOOT/Session/State/Keylogと個人パス・秘密を公開添付しないでください。
