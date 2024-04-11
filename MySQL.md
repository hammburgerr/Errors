# All the errors I faced when I was connecting MySQL to Django

### Error: connect ECONNREFUSED 127.0.0.1:3306
### ERROR (1049, "Unknown database")
### Access denied for user 'root'@'localhost' (using password: YES)
### did you install mysqlclient?

[ Solutions ]
1. I reinstalled MySQL & MySQL workbench
- set a different username and password from the beginning
2. (for MacOS) Settings > MySQL > Initialize Database, Strat MySQL server
3. Made a database in terminal
https://stackoverflow.com/questions/24462007/how-to-deal-with-this-error-1049-unknown-database-users-ohyunjun-work-astra
4. ⭐️ Installed pymysql
https://stackoverflow.com/questions/46902357/error-loading-mysqldb-module-did-you-install-mysqlclient-or-mysql-python

[ Causes ]
1. In VS Code Database, it seems like it can't ***make*** a database. It can only connect with the existing one.
2. Even if I make a database, mysql couldn't make a connection with my db -> it needed pymysql
- This was the main reason the error kept popping up. There wasn't a database but I was making a connection there
