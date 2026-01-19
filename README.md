# cleanup-node-modules

windows向け：一定期間更新していないプロジェクトのnode_modulesを削除するPowerShellスクリプト<br>

https://note.affi-sapo-sv.com/nodejs-delete-nodemodules.php<br>
フォルダ内の複数プロジェクトからnode_modulesを検索して、プロジェクト内のファイルを14日以上更新していないときnode_modulesを削除する。

---

## 使用方法1

1) 全てのファイルを対象フォルダ内に配置<br>
2) check_node_modules.batを実行して、削除候補のnode_modulesを確認<br>
3) cleanup_node_modules.batを実行してnode_modulesを削除<br>

## 使用方法2

次の引数を指定して、check_node_modules.batまたはcleanup_node_modules.batを実行

-delete 削除モード<br>
-d 対象日数（1以上）デフォルト：14<br>
-f 対象フォルダ デフォルト：現在のフォルダ<br>
-force 確認しないで削除<br>
-h ヘルプ表示<br>

※cleanup_node_modules.batは-delete指定済み

## 使用方法3

使用方法2の引数を使用して、cleanup_node_modules.ps1（PowerShellスクリプト）を実行

例：<br>
(Windows PowerShell)<br>
powershell -File cleanup_node_modules.ps1 -delete<br>

または

(PowerShell バージョン6以降)<br>
pwsh -File cleanup_node_modules.ps1 -delete<br>

## 作者

名前: kchan<br>
GitHub: https://github.com/kchan-p/<br>
Website: https://note.affi-sapo-sv.com/<br>

## ライセンス

MIT License<br>