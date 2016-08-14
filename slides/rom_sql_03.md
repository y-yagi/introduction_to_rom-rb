
## rom-sql

* associationsが使える
  * `belongs_to`、`has_many`、`has_many-through`、`has_one`、`has_one-through`

```ruby
class Users < ROM::Relation[:sql]
  schema(infer: true) do
    associations do
      has_many :tasks
      has_one :account
    end
  end
end
```

