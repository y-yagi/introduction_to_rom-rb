
## Schemas

* `rom-sql`の場合、DBのtypeをそのまま使用する事も出来る
  * primary keyやforeign keyの情報もそのまま反映される

```ruby
require 'rom-sql'

class Users < ROM::Relation[:sql]
  schema(infer: true)
end
```
