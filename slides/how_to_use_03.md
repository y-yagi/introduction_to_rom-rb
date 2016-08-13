
## 使い方(`rom-sql`)

まずはmigration

```ruby
require 'rom-repository'
require 'rom-sql'

# `ROM::Configuration`を使用して接続先を指定
conf = ROM::Configuration.new(:sql, 'sqlite::memory')

migration = conf.gateways[:default].migration do
  change do
    create_table(:users) do
      primary_key :id
      column :name, String, null: false
      column :email, String, null: false
    end
  end
end

# migration実行
migration.apply(conf.gateways[:default].connection, :up)
```
