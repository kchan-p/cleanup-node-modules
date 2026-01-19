# cleanup-node-modules

windows向け：一定期間更新していないプロジェクトのnode_modulesを削除するPowerShellスクリプト<br>

https://note.affi-sapo-sv.com/cleanup-node-modules.php<br>
フォルダ内の複数プロジェクトからnode_modulesを検索して、プロジェクト内のファイルを14日以上更新していないときnode_modulesを削除する。

---

## 使用方法

使用方法１：

1) 全てのファイルを対象フォルダ内に配置<br>
2) check_node_modules.batを実行して、削除候補のnode_modulesを確認<br>
3) cleanup_node_modules.batを実行してnode_modulesを削除<br>

使用方法２：

次の引数を指定して、check_node_modules.batまたはcleanup_node_modules.batを実行

-delete 削除モード
-d 対象日数（1以上）デフォルト：14
-f 対象フォルダ デフォルト：現在のフォルダ
-force 確認しないで削除
-h ヘルプ表示

※cleanup_node_modules.batは-delete指定済み

使用方法３：

使用方法３の引数を使用して、cleanup_node_modules.ps1（PowerShellスクリプト）を実行

例：
(Windows PowerShell)
powershell -File cleanup_node_modules.ps1 -delete

または
(PowerShell バージョン6以降)
pwsh -File cleanup_node_modules.ps1 -delete

## 作者

名前: kchan<br>
GitHub: https://github.com/kchan-p/<br>
Website: https://note.affi-sapo-sv.com/<br>

## ライセンス

MIT License<br>