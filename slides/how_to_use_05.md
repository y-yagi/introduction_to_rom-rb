
## 使い方(`rom-sql`)

最後に`Repository`を定義

```ruby
class UserRepo < ROM::Repository[:users]
  commands :create, update: :by_id, delete: :by_id

  def [](id)
    users.by_id(id).one!
  end

  def all
    users.to_a
  end
end
```
