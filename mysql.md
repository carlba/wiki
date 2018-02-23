# Ubuntu

## Reset password

``` bash
sudo dpkg-reconfigure mysql-server-5.5
```

# Usage

# Dump contents of data including data

```
mysqldump -u root -p[password] [database_name] > [dump_file_name].sql
```
˜
# Insert data from dump into database
```
mysql -u root -p [database_name] < [dump_file_name].sql
```