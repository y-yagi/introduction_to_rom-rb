
## 使い方

* READING
  * `Repository`を使用して読み込み処理を発行する
    * `Repository`から更に各`Adapter`が提供する`Relation`を経由して、datastoreからデータの読み込みを行う
* WRITING
  * `Command`を使用して、データのCreate / Update / Deleteを行う
  * 各datastore固有の処理は`Relation`を経由して実行する
