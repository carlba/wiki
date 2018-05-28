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

# Understanding
Use the [online exploratory tool](https://www.w3schools.com/sql/trysql.asp?filename=trysql_op_or) to try out simple SQL queries.

## What is a Database

* A collection of data
  It could be any structured collection of data. It normally has a searchable index.

* A method for accessing and modifying data
  


  







 






