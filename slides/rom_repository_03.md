
## rom-repository

* データの読み込みは`Repository`経由で行う

```ruby
# `users` tableがある場合
class UserRepo < ROM::Repository[:users]
end

# `Repository`を作成する際に、containerを指定する
user_repo = UserRepo.new(rom)
```
