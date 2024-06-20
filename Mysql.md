# MySql

## Remove ONLY_FULL_GROUP_BY (Sql mode) temp

```mysql
	SET GLOBAL sql_mode=(SELECT REPLACE(@@sql_mode,'ONLY_FULL_GROUP_BY',''));

```

## Remove ONLY_FULL_GROUP_BY (Sql mode) permanent


```mysql
	SET PERSIST sql_mode=(SELECT REPLACE(@@sql_mode,'ONLY_FULL_GROUP_BY',''));

```


