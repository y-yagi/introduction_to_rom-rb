
## ROM

* READING
  * アプリは、`Repository`を使用して読み込み処理を発行する
    * 実際は、各`Adapter`が提供する`Relation`を使用して、datastoreから実際のデータの読み込みを行う
* WRITING
  * `Command`を使用して、データのCreate / Update / Deleteを行う

