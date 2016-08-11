
## rom-sql

* `ROM::Container`クラスでDBへの接続情報を管理する

```ruby
rom = ROM.container(:sql, 'sqlite::memory')
```

* `.container`メソッドの第二引数に接続先情報を指定する
  * PostgreSQLの場合`postgres://localhost/rom_sql`、MySQLの場合`mysql2://root@localhost/rom_sql`
