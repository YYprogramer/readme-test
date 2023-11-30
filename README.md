# URLとは
**URLとは情報の住所！**<br>

ある情報が「どこにあるのか」「どんなファイル名なのか」を示しています。<br>

例えばGoogleの検索画面は
https://www.google.com/
と表現されます。これは<br>
```
https = 通信プロトコル
www.google.com = ホスト名
/ = パス
```
と読み下すことができます。<br>
これは「`www.google.com`」というフォルダの「`/`」というページを表示してくださいね。その時の情報をやり取りする方法は「`https`」というルールに従ってくださいね。<br>
ということです。<br>
　　
　　
# クエリ文字列とは
**URLにくっつく命令文**<br>

クエリ文字列は、ウェブページのURLに追加されるデータの一部で、主に検索エンジンやウェブサイトに対して特定の情報を送信するために使用されます。クエリ文字列は、URLの末尾に「?」で始まり、その後にキーと値のペアが「キー=値」の形式で続きます。複数のキーと値がある場合は、「&」で区切ります。<br>

例えばGoogleで「阿部寛」を検索する場合
`https://www.google.com/search?q=阿部寛`となります。<br>
上記の場合「キー」が`q`,「値」が`阿部寛`となります。<br>
また「阿部寛」「爆速ホームページ」と二つの値で検索したい場合は
`https://www.google.com/search?q=阿部寛&爆速ホームページ`となります。<br>
上記の場合「値」が`阿部寛`と`爆速ホームページ`の２つになっています。　　
　　
  
　　
# パス変数（パスパラメータ）とは
**URLに含まれる変数**<br>

パスパラメータは、ウェブページやアプリケーションが特定の情報を取得するためにURLに含まれている情報です。ユーザーごとに異なるページやデータを表示するときに、このパスパラメータを使ってそれぞれのユーザーを区別します。<br> 

例えばインスタグラムのトップページが下記のようなURLだった場合<br>
```
https://instagram.com/ユーザー名/
```
この`ユーザー名`部分がパス変数となります。<br>
具体的には<br>
`https://instagram.com/abe_hiroshi/`と入力すると阿部寛さんのインスタトップページが<br>
`https://instagram.com/nakama_yukie/`と入力すると仲間由紀恵さんのインスタトップページが<br>
それぞれ表示されます。※あくまで例え話です。
　　
  
　　
# クエリ文字列とパス変数の違い
**クエリ文字列は検索に使用。パス変数は特定のリソースにアクセスするために使用**<br>
- 同意点<br>
どちらもURLに記述されている  
- 相違点<br>
クエリ文字列は、URLの末尾に「？」で始まり、「key=value」の形式でデータを伝達するため、主に検索機能として使用される。　　
パス変数は、URLの一部をユーザーごとに変える変数として管理し、ユーザーに合わせて動的にサイトを管理する際に使用される。
　　
　　
# HTTPメソッドとは
**クライアント側からサーバー側に送られる命令**　　

ウェブサイトを閲覧する場合、自分のパソコン（クライアント）からデータを保存している場所（サーバー）に「そのサイトを見せて」という命令が出されます。  
この命令のことをHTTPメソッドと言います。命令には下記の種類があります。

| HTTPメソッド名 | 内容 |
|---|---|
|get| サーバーから情報を取得する命令。Webサイトを表示させるときに使用 |
|post| サーバーに新しい情報を送る命令。コメントを投稿するときに使用 |
|put| サーバー上の情報を更新する命令。投稿を修正するときに使用 |
|patch|  サーバー上にある情報を一部更新する命令。投稿を一部修正するときに使用|
|delete| サーバー上の情報を削除する命令。投稿を削除するときに使用 |　　

　　
  
# リクエストヘッダとは 
**HTTPリクエストに含まれるあれやこれやの情報**　　

Webサイトを閲覧するにはクライアントからサーバーへ命令が送られます。この命令は`HTTPリクエスト`と呼ばれます。  
このHTTPリクエストは`リクエストライン`、`リクエストヘッダ`、`メッセージボディ`の３つで構成されています。  
このうち`リクエストヘッダ`には<br>
`HOST` サーバーサイドのドメイン名<br>
`User-Agent` リクエストを送信したホスト側の情報<br>
などが含まれています。
  
  
  
#　HTTPステータスとは
**HTTPリクエストに対する処理結果**　　

クライアントおよびサーバーが、HTTPリクエストに対する処理結果を示す3桁の数字です。処理結果としては下記のものがあります。
| HTTPリクエストステータスコード | 内容 |
| --- | --- |
| 200 |  リクエストが成功。 |
| 201 |  リクエストが成功し、新しい情報が作成された。例えばPostメソッドのリクエストが成功 |
| 400 |  リクエストが無効である。例えばリクエストがサーバの期待する値ではない |
| 404 |  リクエストは失敗。例えばリクエストされたURLが存在しない |
| 500 |  サーバー側での問題により、リクエスト失敗 |
