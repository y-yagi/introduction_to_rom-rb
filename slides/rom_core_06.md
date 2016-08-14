
## Schemas

* attributeの名前と型を定義する為の仕組み
* schemaはRelationクラスの中に定義する

```ruby
class Users < ROM::Relation[:http]
  schema do
    attribute :id, ROM::Types::Int
    attribute :name, ROM::Types::String
    attribute :age, ROM::Types::Int
  end
end
```

