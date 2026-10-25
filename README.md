# GunSwan — developed by さっち

Copyright © 2026 さっち。個人開発のWindows x64向けWonderSwan / WonderSwan Color / SwanCrystalエミュレーターです。

## ダウンロード — Windows v1.0.1

**[GunSwan v1.0.1 Windows x64 ZIP](https://github.com/yosisato-boop/GunSwan-Releases/releases/download/v1.0.1/GunSwan-1.0.1-license-r1-windows-x64.zip)**

- [正式Release・公開日時](https://github.com/yosisato-boop/GunSwan-Releases/releases/tag/v1.0.1) / [SHA-256と導入](DOWNLOAD.md)
- [変更点・1.0.1正式日本語LICENSE](GUNSWAN_V1_0_1_RELEASE_NOTES_JA.md)
- ZIP SHA-256: `73ce80cef6bd3995a7863a846c12bdba81abada27b99bb0755e115a50df77e00`

Finallyの文字変形表示とRaster Paletteの汎用描画、クロノアのセーブ一覧文字欠落を修正しました。検証対象をOwned52へ拡張しました。Tare Pandaの分類低下、旧SessionのStrict NonExact、物理Palette fetch位相などの制限を維持します。全タイトルの完全互換性は保証しません。

利用条件はZIP内LICENSE.txtと[同一の日本語正文](GUNSWAN_V1_0_1_RELEASE_NOTES_JA.md#license)です。公開名義はさっち。正式一般配布開始日はReleaseの実際の公開日時によります。v1.0.0のtag・Release・ZIPは保持します。

## 過去の版 — Windows v1.0.0

**[GunSwan v1.0.0 をダウンロード（Windows x64 ZIP）](https://github.com/yosisato-boop/GunSwan-Releases/releases/download/v1.0.0/GunSwan-1.0.0-license-r1-windows-x64.zip)**

- [正式リリースページ（更新内容・配布記録）](https://github.com/yosisato-boop/GunSwan-Releases/releases/tag/v1.0.0)
- [SHA-256の確認方法・必要環境・導入手順](DOWNLOAD.md)

正式公開：2026年10月17日 22:05:56（日本時間）。配布ファイル：`GunSwan-1.0.0-license-r1-windows-x64.zip`。
GitHubの「Source code (zip / tar.gz)」は案内文書のみです。実行ファイルは上記の配布ZIPを取得してください。

### はじめて使う方へ

Windows x64とMicrosoft Visual C++ v14 Redistributable x64が必要です。
最小対応Windows版は未確定です。Windows 11開発環境と別PCでの機能確認があり、全環境の動作保証はありません。
Runtimeの入手先と詳しい操作は[導入・操作](INSTALL.md)、制約は[既知の制約](KNOWN_ISSUES.md)を参照してください。

1. 配布ZIPをダウンロードし、[SHA-256を確認](DOWNLOAD.md#sha-256の確認方法)します。
2. ZIPを展開し、GunSwanフォルダー内のファイルをまとめて保持します。
3. `gunswan-launcher.exe`を起動し、自身で用意した `.ws` / `.wsc` ROMを指定して「START GUNSWAN」を選びます。

ROMは同梱していません。通常プレイにFFmpegは不要です。Movie出力には別途FFmpegが必要です。

## 利用条件・関連文書

無料の個人・家庭・教育研究・企業内通常利用、必要コピー・backup、限定ローカル解析を認める正式条件を所有者承認済み。
第三者再配布・ミラー・本体販売・商用組込みは個別許可制です。詳細は日本語正文に従います。
このリポジトリは公開案内文書専用で、製品ソース・開発Git履歴を含みません。
GitHub自動Source code archiveはこの案内文書だけです。公開用tagと開発v1.0.0タグは別履歴です。

- [ダウンロードとSHA](DOWNLOAD.md) / [利用条件](USAGE_POLICY.md) / [最新1.0.1日本語LICENSE](GUNSWAN_V1_0_1_RELEASE_NOTES_JA.md#license)
- [導入・操作](INSTALL.md) / [最新Release notes](GUNSWAN_V1_0_1_RELEASE_NOTES_JA.md) / [既知制約](KNOWN_ISSUES.md)
- [第三者条件](THIRD_PARTY.md) / [文書条件](LICENSE.md) / [セキュリティ](SECURITY.md)

一般問い合わせ・不具合・互換性・利用質問・要望・文書不備はGitHub Issues、日本語中心で英語も受け付けます。
個人メールや本名は要求しません。ROM/BOOT/私的Session/State/Keylog/秘密を添付しないでください。
非公開脆弱性報告はPrivate Vulnerability Reportingを採用し、公開前に入口と管理者通知を確認します。
非公開報告の入口が表示されない場合、秘密を含まない一般的な窓口確認だけをIssuesへ記載し、詳細は非公開経路の確認後に送ってください。
