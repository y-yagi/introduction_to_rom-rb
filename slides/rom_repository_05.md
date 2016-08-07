
## rom-repository

* 特定のclassにマッピングしたい場合、`as`メソッドを使用する


```ruby
class User
  attr_reader :id, :name, :email

  def initialize(attributes)
    @id, @name, @email = attributes.values_at(:id, :name, :email)
  end
end

user_repo.users.where(name: 'Malcolm').as(User).to_a
#=> [#<User:0x00558d6b762f20 @email="malcolm@example.com", @id=1, @name="Malcolm]
# `User`クラスのArrayになる
```
