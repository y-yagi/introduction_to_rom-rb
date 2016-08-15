
## rom-sql

* データの取得は`where`で

```ruby

require 'rom-sql'

class Users < ROM::Relation[:sql]
  schema(infer: true)

  def by_id(id)
    where(id: id)
  end
end

container = ROM.container(:sql, 'sqlite::memory') do |conf|
  conf.default.connection.create_table(:users) do
    primary_key :id
    column :name, String, null: false
    column :email, String, null: false
  end

  conf.register_relation(Users)
end

container.relations.users.insert(name: "Malcolm", email: "malcolm@example.com")

puts container.relations.users.where(id: 1)
```
* `first`や`last`なども使える
