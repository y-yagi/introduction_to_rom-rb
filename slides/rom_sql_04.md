
## rom-sql

* 複数DBも対応可能

```ruby
ROM.container(
  default: [:sql, 'postgres://localhost/task_master'], # gateway 1
  legacy: [:sql, 'mysql2://localhost/tasks']           # gateway 2
) do |rom|
    ...
end
```
