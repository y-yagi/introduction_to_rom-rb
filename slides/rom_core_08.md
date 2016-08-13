
## Schemas

* rom共通で使用出来る型は`ROM::Types` namespaceで提供されている
* RDBMS固有の型等は別のnamespace(ex: `ROM::SQL::Types::PG`)で提供されている

```ruby
require 'rom-sql'
require 'rom/sql/types/pg'

class Users < ROM::Relation[:sql]
  schema do
    attribute :meta, ROM::SQL::Types::PG::JSON
    attribute :tags, ROM::SQL::Types::PG::Array
    attribute :info, ROM::SQL::Types::PG::Hash
  end
end
```
