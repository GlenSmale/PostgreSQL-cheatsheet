# PostgreSQL-cheatsheet
A Quickref cheatsheet for PostgreSQL

## Get started
### Connect as postgres user
<em>Run in terminal</em>
```
sudo -u postgres psql
```

### List all databases
<em>Run in psql console</em>
```
postgres=# \l
```

### Connect to the database named postgres
<em>Run in psql console</em>
```
postgres=# \c postgres
```

### Disconnect
<em>Run in psql console</em>
```
postgres=# \q
postgres=# \!
```

## Permissions
<em>Run in terminal</em>
```
sudo su - postgres
psql
```

## Grant all permissions on database
```
GRANT ALL PRIVILEGES ON DATABASE <db_name> TO <user_name>;
```

## Grant connection permissions on database
```
GRANT CONNECT ON DATABASE <db_name> TO <user_name>;
```

## Grant permissions on schema
```
GRANT USAGE ON SCHEMA public TO <user_name>;
```

## Grant permissions to functions
```
GRANT EXECUTE ON ALL FUNCTIONS IN SCHEMA public TO <user_name>;
```

## Grant permissions to select, update, insert, delete, on a all tables
```
GRANT SELECT, UPDATE, INSERT ON ALL TABLES IN SCHEMA public TO <user_name>;
```

## Grant permissions, on a table
```
GRANT SELECT, UPDATE, INSERT ON <table_name> TO <user_name>;
```

## Grant permissions, to select, on a table
```
GRANT SELECT ON ALL TABLES IN SCHEMA public TO <user_name>;
```
