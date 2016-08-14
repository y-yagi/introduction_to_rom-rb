
## romとRails

* rom用のinitializerを作成して、DBの接続先を指定する

```ruby
# config/initializers/rom.rb
ROM::Rails::Railtie.configure do |config|
  config.gateways[:default] = [:sql, ENV.fetch('DATABASE_URL')]
end
```

