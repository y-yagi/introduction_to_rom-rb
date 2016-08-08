
## Relations

```ruby
class Users < ROM::Relation[:sql]
end
```

上記は

* adapterに`rom-sql`を使用する
* `users`という名前の`dataset`にアクセスする為のクラス

という事を宣言している
