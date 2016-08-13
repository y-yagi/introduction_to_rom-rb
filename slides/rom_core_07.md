
## Schemas

* primary keyやforeign keyも使える

```ruby
class Users < ROM::Relation[:http]
  schema do
    attribute :id, ROM::Types::Int
    attribute :name, ROM::Types::String
    attribute :age, ROM::Types::Int

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
