If you would like to prepopulate your database with the schema or the data, make a dump file using pg_dump meant for postgres sql

The command is :
```bash
pg_dump -U postgres docker-test > C:\Users\<username>\OneDrive\Desktop\<dbname>_backup_latest.sql
```