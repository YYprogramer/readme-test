# URLとは
**URLとは情報の住所！**<br>
ある情報が「どこにあるのか」「どんなファイル名なのか」を示しています。<br>
例えばGoogleの検索画面は
https://www.google.com/
と表現されます。これは<br>
`https` = 通信プロトコル<br>
`www.google.com` = ホスト名<br>
`/` = パス<br>
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
パスパラメータは、ウェブページやアプリケーションが特定の情報を取得するためにURLに含まれている情報ですす。ユーザーごとに異なるページやデータを表示するときに、このパスパラメータを使ってそれぞれのユーザーを区別します。<br> 
例えばインスタグラムのトップページが下記のようなURLだった場合<br>
`https://instagram.com/ユーザー名/`<br>
この`ユーザー名`部分がパス変数となります。<br>
具体的には<br>
`https://instagram.com/abe_hiroshi/`と入力すると阿部寛さんのインスタトップページが<br>
`https://instagram.com/nakama_yukie/`と入力すると仲間由紀恵さんのインスタトップページが<br>
それぞれ表示されます。※あくまで例え話です。

