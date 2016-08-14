
## 使い方(`rom-sql`)

次に`Relation`クラスを作成

```ruby
conf = ROM::Configuration.new(:sql, 'sqlite::memory')

# Relation
class Users < ROM::Relation[:sql]
  schema(infer: true)

  def by_id(id)
    where(id: id)
  end
end

# ROM::ConfigurationにRelationを登録
conf.register_relation(Users)

# ROM::Configurationを使用してROM::Containerを作成する
rom = ROM.container(conf)
```
