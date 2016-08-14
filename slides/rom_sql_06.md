
## rom-sql

* 作成 / 更新 /削除は`Relation`を使用して行う
  * 実際の処理は`Command`を使用して行われている

```ruby
container.relations.users.insert(name: "Malcolm", email: "malcolm@example.com")
container.relations.users.where(id: 1).update(name: "first")
```
