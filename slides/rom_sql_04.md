
## rom-sql

* Joinも使える

```ruby
class Users < ROM::Relation[:sql]
  def with_tasks
    inner_join(:tasks, user_id: :id)
  end

  def with_posts
    left_join(:posts, user_id: :id)
  end
end
```
