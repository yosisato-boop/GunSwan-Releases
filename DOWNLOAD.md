# GunSwan v1.0.0 のダウンロード

**[Windows x64向け正式配布ZIPをダウンロード](https://github.com/yosisato-boop/GunSwan-Releases/releases/download/v1.0.0/GunSwan-1.0.0-license-r1-windows-x64.zip)**

- [正式リリースページ（更新内容・配布記録）](https://github.com/yosisato-boop/GunSwan-Releases/releases/tag/v1.0.0)
- 配布ファイル：`GunSwan-1.0.0-license-r1-windows-x64.zip`
- Application version：1.0.0 / package revision：license-r1 / developed by さっち
- 正式一般配布開始：2026年10月17日 22:05:56（日本時間） / 2026-10-17T13:05:56Z（UTC）

GitHubの「Source code (zip / tar.gz)」は公開案内文書だけで、製品ソースや実行ファイルではありません。
上記の同名ZIPをダウンロードしてください。

## 必要な動作環境

- Windows x64
- Microsoft Visual C++ v14 Redistributable x64（自動導入・同梱はしません）。
  [Microsoft公式Runtime案内](https://learn.microsoft.com/en-us/cpp/windows/latest-supported-vc-redist?view=msvc-170)でx64用を確認してください。
- 自身で用意した `.ws` / `.wsc` ROM（配布ZIPには同梱しません）。

Windows 11開発環境と別PCでの機能確認はありますが、別PCのOS/Runtime詳細は未記録です。
最小対応Windows版や全driverでの動作は保証していません。[既知の制約](KNOWN_ISSUES.md)も確認してください。
Movie出力には別途FFmpegが必要です。通常プレイには不要です。詳細は[導入・操作](INSTALL.md)を参照してください。

## SHA-256の確認方法

ダウンロードした**ZIPを展開する前に**、SHA-256が次の値と一致することを確認してください。

```text
23de407530ca34a264b9e92267a9b0c22f5d57177ce1abe28957fda8a147f15a
```

エクスプローラーでZIPを保存したフォルダーを開き、アドレスバーに `powershell` と入力してEnterを押します。
開いたPowerShellで、次を実行してください。

```powershell
Get-FileHash -LiteralPath ".\GunSwan-1.0.0-license-r1-windows-x64.zip" -Algorithm SHA256
```

表示された `Hash` の64桁すべてが上記の値と一致すれば確認完了です（英字の大文字・小文字は問いません）。
一致しない場合は起動せず、上記の公式リンクから再取得してください。
再取得後も一致しない場合は[Issues](https://github.com/yosisato-boop/GunSwan-Releases/issues)へ報告してください。

同じZIP SHA-256は[正式リリース本文](https://github.com/yosisato-boop/GunSwan-Releases/releases/tag/v1.0.0)にも記載されています。
確認対象はZIP自体です。展開した実行ファイルや「Source code」のSHA-256とは異なります。

## 導入・起動

1. [正式日本語LICENSE](GUNSWAN_BINARY_LICENSE_JA.md)と[利用条件](USAGE_POLICY.md)を確認します。
2. ダウンロードしたZIPのSHA-256を上記の方法で照合し、ZIPを展開します。
3. 展開したGunSwanフォルダー内のファイルを一緒に保持します。
4. `gunswan-launcher.exe`を起動し、自身の `.ws` / `.wsc` ROMを指定して「START GUNSWAN」を選びます。

Runtime不足・不足DLLのエラーが出る場合は[導入・操作](INSTALL.md)を参照し、Microsoft公式のx64 Runtimeを確認してください。
第三者のDLL単体配布サイトから取得しないでください。
キー設定、ゲームパッド、保存、Session Viewer、Movie出力の説明も[導入・操作](INSTALL.md)にあります。

## ライセンス・配布記録

[正式日本語LICENSE](GUNSWAN_BINARY_LICENSE_JA.md)のSHA-256：
`2ffc9e434a4a38ecc0622fa58573ad31f5ea84e023934f4727d09f70fbb40530`。

正式な一般配布開始日から適用し、日付・公式配布URL・対象ZIP/LICENSE SHAは
[正式リリースの配布記録](https://github.com/yosisato-boop/GunSwan-Releases/releases/tag/v1.0.0)で確認できます。

元製品の旧ZIP（SHA `697576d2e1b75ebf0bdd9f68831048650588ff257aeb0a11570b84b785bc3ce9`）とは別の文書・ライセンスrevisionです。
今回のダウンロード確認には、このページ上部に記載した正式配布ZIPのSHA-256を使用してください。
