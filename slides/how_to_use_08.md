
## 使い方

* データの操作は`Repository`を使用して行う
* `Repository`はデータに操作する抽象的な操作のみ行い、datastoreに対する具体的な処理は`Relation`で行う
  * これは推奨されている(おそらく)だけで、実際は`Repository`を経由せずに`Relation`を直接使用する事も出来る
* `Repository`にdatastoreに対する具体的な処理を定義しない事で、仮にdatastoreが変わっても`Relation`を差し替えるだけで同じAPIを使用出来る
  * ようにしたいと思われる