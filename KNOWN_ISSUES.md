# v1.0.1の既知制約

- Tare Pandaは受理済み参照でM13→M12へ分類低下しています。
- Tokyo Majin / Klonoaの旧SessionはStrict NonExactです。Terrors 2 / Crazy ClimberのExactと区別し、再記録で過去の不一致が修復された扱いにはしません。
- 物理Palette fetch位相は未確定です。Last Aliveの境界画素、命令完了/fetch0暫定モデル、未知State prefixの表示履歴不足を残します。

- 全タイトル・全Windows版・全GPU/音声デバイスの互換性保証はありません。
- v1.0.0の別PC10項目合格は過去の証拠であり、1.0.1のClean Windows依存関係試験ではありません。OS/Runtime等の詳細は未記録です。
- Viewerのslow/高速の全聴感、高速倍率の完全達成、長区間・全device安定性は未認定です。
- Device recoveryは採用済みですが、全driver・sleep/RDPでの無停止を保証しません。
- legacy Session v2には過去実行とのExact不一致が残る場合があります。
  V3再記録やBestEffort Movieが昔のExact不一致を修復したことにはなりません。
- LCD表示は近似で、実機パネル全個体の測定再現ではありません。
- 通信RX/link cable、Flash Recovery、iOSは対象外です。
- 保存の原子的公開は、物理電源断・全disk-full/UNC条件の完全保証ではありません。
- CLIとWindows PE版情報は1.0.1です。コード署名は未付与です。

正式条件と公開日・対象はLICENSE及び外部Release recordで確認してください。
