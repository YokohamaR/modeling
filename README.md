生態学における統計モデリング（入門）
=====

Rを使った統計モデリングに関する各種情報をまとめます

## RStan

* [Stan](http://mc-stan.org/)をRに実装したもの。	
http://qiita.com/uri/items/2fd051c18a148f7d2a35 に記事を書いたの参考

### 実行例

モデルを記述する`.rstan`という拡張子のファイルとstan実行のための`.R`ファイルを用意する（必ずそうしなければいけないというわけでなく、Rファイル単体にモデルを記述することもできるが、メンテナンスなどの理由から個別のファイルにすることを勧める）。

#### stanファイルの構造

https://github.com/stan-dev/rstan/wiki/RStan-Getting-Started にある`8schools.stan`と`rats.stan`を見てみましょう。.stanファイルは次のような構造を持っていることがわかります

* **data**
* **parameters**
* **transformed parameters**
* **model**
* **generated quantities**

手続き型と呼ばれます。

#### Rでのstanの実行

```{r}
library(rstan)
model <- stan_model() # モデルファイルの読み込み
```

### ドキュメント

公式ページに各種ドキュメントがあるのでどうぞ

* [Manual](http://mc-stan.org/manual.html)
* [Example](http://mc-stan.org/examples.html)