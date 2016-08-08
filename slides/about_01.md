
## ROM

* ROM: Ruby Object Mapper
* DBのデータとRubyのobjectをマッピングする為のライブラリ
* Active Recordと異なりdatastoreはRDBMSに限定されない
  * datastore毎にgemがある(RDBMS: `rom-sql`、MongoDB: `rom-mongo`等)
  * また、datastoreはDBに限定されていない。Gitを操作する為の`rom-git`、CSVを操作する為の`rom-csv`などもある。
