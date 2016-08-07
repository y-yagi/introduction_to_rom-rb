
## rom-repository

```ruby
# repositoryを経由してデータを取得する

user_repo.users.where(name: 'Malcolm')
# => #<ROM::Repository::RelationProxy:0x0055634cdaaed0

user_repo.users.where(name: 'Malcolm').to_a
#=> [#<ROM::Struct[User] id=1 name="Malcolm" email="malcolm@example.com">]
# デフォルトでは`ROM::Struct`というclassにマッピングされる

user_repo.users.fetch(1)
# => {:id=>1, :name=>"Malcolm", :email=>"malcolm@example.com}
# ただのHash
```
