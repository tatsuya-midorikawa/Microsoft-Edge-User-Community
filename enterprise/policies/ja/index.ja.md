# グループ ポリシー

2024/08 現在、Edge for Desktop のグループ ポリシーは 600 近くの項目が提供されています。600 近くのすべてのグループ ポリシーの項目を精査し、設定・管理をすることは非現実的です。また、すべてのグループ ポリシー (または非常に多くのグループ ポリシー) を構成することで、自社に都合の悪い何らかの問題が生じた場合に、問題を切り分けることが困難となってしまい、解決までに余計な時間を消費する懸念も生じてしまいます。
そのため、通常は自社が制御したい項目に絞ってグループ ポリシーを構成していくことが望ましいです。また、Microsoft より [Microsoft Edge Security Baseline](https://techcommunity.microsoft.com/t5/microsoft-security-baselines/bg-p/Microsoft-Security-Baselines) が提供されているため、それに絞って検討を進めるのも良いかと思います。
いずれにせよ、すべての項目を網羅することを考えるのではなく、必要最低限の項目に絞って適用するグループ ポリシーの検討を進めていくことが肝要です。


## グループ ポリシー の構成戦略

適用するグループ ポリシーを考える前に、前提として Edge はそのままの状態でも十分セキュアです。その状態からさらにセキュリティー レベルを上げるのか、それともセキュリティー レベルを下げるのか、という観点で戦略を練っていきます。Edge のセキュリティーについては [こちらの公式ページ](https://learn.microsoft.com/ja-jp/deployedge/ms-edge-security-for-business) を参考にしてみると良いでしょう。

Edge のセキュリティーをより強固にしたい場合、自社の Web システムや現在利用している他社の Web システム、Web サーバーが最新の Web 標準やセキュリティー機能などに対応しているかが重要になってきます。Enterprise システムにおいては、予算や納期などの都合から Legacy な資産を運用し続けなければならないなどの制約が生じがちです。そのため、Edge のセキュリティー レベルをより厳しくすることで、自社の Web システムが意図通りに動作しなくなる可能性があります。例えば、Microsoft Edge Security Baseline v117 においては `AuthSchemes = "ntlm,negotiate"` となっていますが、自社システムが Basic 認証をいまだに利用し続けている場合、当然許可されていないためその Web システムは動作しなくなります。また `DefaultPopupsSetting = (2)` と設定し、ポップアップ ウィンドウの表示をすべてのサイトで禁止するようにした場合、ポップアップを利用して動作させている Web システムが利用できなくなったりもします。このように無闇にセキュリティー レベルを厳しくしてしまうと正常に Web システムが動作しなくなる危険性があるので、実際にグループ ポリシーを検証環境に適用しつつ、動作検証を進める必要があります。


## 参考情報

- [Microsoft Edge - ポリシー](https://learn.microsoft.com/ja-jp/deployedge/microsoft-edge-policies)
- [Windows デバイスで Microsoft Edge ポリシー設定を構成する](https://learn.microsoft.com/ja-jp/deployedge/configure-microsoft-edge)