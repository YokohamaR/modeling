生態学における統計モデリング（入門）
=====

Rを使った統計モデリングに関する各種情報をまとめます

## RStan

* [Stan](http://mc-stan.org/)をR上で実行できるようにしたインターフェイス。	
http://qiita.com/uri/items/2fd051c18a148f7d2a35 に記事を書いたの参考

### 実行例

モデルを記述する`.rstan`という拡張子のファイルとstan実行のための`.R`ファイルを用意する（必ずそうしなければいけないというわけでなく、Rファイル単体にモデルを記述することもできるが、メンテナンスなどの理由から個別のファイルにすることを勧める）。