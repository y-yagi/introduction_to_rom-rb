
## Schemas

* attributeの名前と型を定義する為の仕組み
* schemaはRelationクラスの中に定義する

```ruby
class Users < ROM::Relation[:http]
  schema do
    attribute :id, Types::Int
    attribute :name, Types::String
    attribute :age, Types::Int
  end
end
```

