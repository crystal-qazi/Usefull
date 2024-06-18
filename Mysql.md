# MySql

## Remove ONLY_FULL_GROUP_BY (Sql mode)

```mysql
	SET GLOBAL sql_mode=(SELECT REPLACE(@@sql_mode,'ONLY_FULL_GROUP_BY',''));

```


