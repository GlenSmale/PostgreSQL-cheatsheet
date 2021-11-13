# PostgreSQL-cheatsheet
Quickref cheatsheet for PostgreSQL database users
<br>
<br>
### Getting Started
<em>Run in terminal</em>
```
sudo -u postgres psql
```

### List all databases
<em>Run in psql console postgres=#</em>
```
\l
```

### Connect to the database named postgres
```
\c postgres
```

### Disconnect
```
\q
\!
```

## Permissions
<em>Run in terminal</em>
```
sudo su - postgres
psql
```

### Grant all permissions on database
<em>Run in psql console postgres=#</em>
```
GRANT ALL PRIVILEGES ON DATABASE <db_name> TO <user_name>;
```

### Grant connection permissions on database
```
GRANT CONNECT ON DATABASE <db_name> TO <user_name>;
```

### Grant permissions on schema
```
GRANT USAGE ON SCHEMA public TO <user_name>;
```

### Grant permissions to functions
```
GRANT EXECUTE ON ALL FUNCTIONS IN SCHEMA public TO <user_name>;
```

### Grant permissions to select, update, insert, delete, on a all tables
```
GRANT SELECT, UPDATE, INSERT ON ALL TABLES IN SCHEMA public TO <user_name>;
```

### Grant permissions, on a table
```
GRANT SELECT, UPDATE, INSERT ON <table_name> TO <user_name>;
```

### Grant permissions, to select, on a table
```
GRANT SELECT ON ALL TABLES IN SCHEMA public TO <user_name>;
```

## Users
### List roles
SELECT rolname FROM pg_roles;

### Create user
```
CREATE USER <user_name> WITH PASSWORD '<password>';
```

### Drop user
```
DROP USER IF EXISTS <user_name>;
```

### Alter user password
```
ALTER ROLE <user_name> WITH PASSWORD '<password>';
```

### Create a new user 
```
CREATE USER <user_name> WITH PASSWORD '<password>';
```

### Alter user with superuser privilege
```
ALTER ROLE <user_name> WITH SUPERUSER;
```

### Revoke user superuser status
```
ALTER ROLE <user_name> WITH NOSUPERUSER;
```

### Drop superuser
```
DROP USER IF EXISTS <user_name>;
```

## Databases
### List databases
```
\l
```

### Connect to database
```
\c <database_name>
```

### Show current database
```
SELECT current_database();
```

### Create database
```
CREATE DATABASE <database_name> WITH OWNER <username>;
```

### Drop database
```
DROP DATABASE IF EXISTS <database_name>;
```

### Rename database
```
ALTER DATABASE <old_name> RENAME TO <new_name>;
```
