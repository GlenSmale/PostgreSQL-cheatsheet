# PostgreSQL-common-errors

### psql: could not connect to server: No such file or directory
```
psql
```
>psql: could not connect to server: No such file or directory
    Is the server running locally and accepting
    connections on Unix domain socket "/tmp/.s.PGSQL.5432"?
    
### Fix with:
<em>Run in terminal</em>
```
brew services stop postgresql
rm /usr/local/var/postgres/postmaster.pid
brew services start postgresql
```


