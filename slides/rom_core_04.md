
## Relations

```ruby
class Users < ROM::Relation[:sql]
end
```

上記の場合

* adapterに`rom-sql`を使用する
* `users`という名前の`dataset`にアクセスする為のクラス

になる
