# MySQL 

* When mysqldump fails with the error message

  `  mysqldump: [ERROR] unknown variable 'set-variable=max_allowed_packet=100M'`

  on the command line, the parameter `--defaults-file` has to be set:

  `  mysqldump --defaults-file=C:\MySQL\my.ini -uusername -ppassword databasename >Dump.sql`
  
* A column that is case insensitive can be queried in a case sensitive way using the keyword `binary` in MySQL:

  `  select bar from foo where binary bar = 'qux'`  
  
* How to temporarily disable foreign key constraint checks in MySQL:

  `  set foreign_key_checks = 0;`

  `  // Delete stuff`

  `  set foreign_key_checks = 1;`
