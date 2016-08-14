
## romとRails

* 後は先ほどのサンプル同様`Relation`や`Repository`を定義すればOK

```ruby
# app/relations/users.rb
class Users < ROM::Relation[:sql]
end
```

```
ROM.env.relations[:users]
#=> #<Users dataset=#<Sequel::SQLite::Dataset: "SELECT * FROM `users`">>
```
