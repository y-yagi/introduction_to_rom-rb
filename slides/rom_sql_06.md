
## rom-sql

* 作成 / 更新 /削除は`Relation`を使用して行う
  * 実際使用する場合は、`Repository`を経由し、`Command`を使用して処理を行う事が推奨されている(はず)

```ruby
container.relations.users.insert(name: "Malcolm", email: "malcolm@example.com")
container.relations.users.where(id: 1).update(name: "first")
```
