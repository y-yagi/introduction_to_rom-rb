
## 使い方(`rom-sql`)

次に`Relation`を定義、及び登録

```ruby
conf = ROM::Configuration.new(:sql, 'sqlite::memory')

# Relation
class Users < ROM::Relation[:sql]
  schema(infer: true)

  def by_id(id)
    where(id: id)
  end
end

# `ROM::Configuration`に`Relation`を登録
conf.register_relation(Users)

# `ROM::Configuration`を使用して`ROM::Container`を作成する
rom = ROM.container(conf)
```
