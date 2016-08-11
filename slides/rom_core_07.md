
## Schemas

* primary keyやforeign keyも使える

```ruby
class Users < ROM::Relation[:http]
  schema do
    attribute :id, Types::Int
    attribute :name, Types::String
    attribute :age, Types::Int

    primary_key :id
  end
end
```

```ruby
class Posts < ROM::Relation[:http]
  schema do
    attribute :user_id, Types::ForeignKey(:users)
  end
end
```
