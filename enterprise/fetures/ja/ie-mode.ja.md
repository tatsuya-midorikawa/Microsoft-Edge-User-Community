# Edge (IE モード)

Edge (IE モード) は、IE11 の EOS までに Edge などのモダン ブラウザーへの改修・移行作業が間に合わなかった企業向けに提供された機能となります。また 2024/08/16 時点においては [2029年までのサポート](https://blogs.windows.com/japan/2022/02/21/internet-explorer-11-desktop-app-retirement-faq/#:~:text=IE%20%E3%83%A2%E3%83%BC%E3%83%89%E3%81%AF%E3%81%84%E3%81%A4%E3%81%BE%E3%81%A7%E3%82%B5%E3%83%9D%E3%83%BC%E3%83%88%E3%81%95%E3%82%8C%E3%81%BE%E3%81%99%E3%81%8B%EF%BC%9F) となっているため、それまでにはモダン ブラウザーへの移行対応が必要となります。

Edge (IE モード) は、管理者によって設定する **Enterprise mode sitelist** 方式か、各ユーザーで独自に設定できる **Local sitelist** 方式、またはユーザー操作による **IE モードで再読み込み** のいずれかによって利用できます。


## Enterprise mode sitelist (エンタープライズ モード サイトリスト) 方式

Enterprise mode sitelist 方式は、管理者が作成するサイトリスト (.XML ファイル) で指定したサイトのブラウザー エンジン (Edge Native モードか IE モードか) を管理する方法です。
サイトリストでブラウザー エンジンとして Edge (IE モード) を指定したサイトは、サイト アクセス時に Edge (IE モード) でページが開かれるようになります。

### 設定手順

1. サイトリスト (.XML ファイル) を作成する - [Enterprise Mode schema v.2 guidance](https://learn.microsoft.com/en-us/previous-versions/windows/internet-explorer/ie-it-pro/internet-explorer-11/ie11-deploy-guide/enterprise-mode-schema-version-2-guidance)
1. 


## 参考情報

- [Internet Explorer (IE) モードとは - Microsoft Learn](https://learn.microsoft.com/ja-jp/deployedge/edge-ie-mode)
- [Internet Explorer 11 デスクトップ アプリケーションのサポート終了](https://blogs.windows.com/japan/2022/02/21/internet-explorer-11-desktop-app-retirement-faq/#:~:text=IE%20%E3%83%A2%E3%83%BC%E3%83%89%E3%81%AF%E3%81%84%E3%81%A4%E3%81%BE%E3%81%A7%E3%82%B5%E3%83%9D%E3%83%BC%E3%83%88%E3%81%95%E3%82%8C%E3%81%BE%E3%81%99%E3%81%8B%EF%BC%9F)