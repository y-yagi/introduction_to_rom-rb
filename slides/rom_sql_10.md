
## `Command`

* 普通にクラスなので、独自の`Command`クラスを作成する事も可能

```ruby
class UpsertUser < ROM::Commands::Create[:sql]
  relation :users
  register_as :upsert

  def execute
     # do the operations to create a new record or update an existing one
  end
end
```
