
## 使い方(`rom-sql`)

`Repository`を使用して、データの操作を行う

```ruby
# ROM::ContainerをRepositoryのインスタンス生成時に指定する
user_repo = UserRepo.new(rom)

user = user_repo.create(name: 'Jane', email: 'jane@doe.org')
puts user.inspect
# => #<ROM::Struct[User] id=1 name="Jane" email="jane@doe.org">

puts user_repo.all.inspect
# => [#<ROM::Struct[User] id=1 name="Jane" email="jane@doe.org">]

user_repo.update(user.id, name: 'Jane Doe')
puts user_repo[user.id].inspect
# => #<ROM::Struct[User] id=1 name="Jane Doe" email="jane@doe.org">

user_repo.delete(user.id)
```
