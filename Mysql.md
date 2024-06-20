# MySql

## Remove ONLY_FULL_GROUP_BY (Sql mode) temp

```mysql
	SET GLOBAL sql_mode=(SELECT REPLACE(@@sql_mode,'ONLY_FULL_GROUP_BY',''));

```

## Remove ONLY_FULL_GROUP_BY (Sql mode) permanent


```mysql
	SET PERSIST sql_mode=(SELECT REPLACE(@@sql_mode,'ONLY_FULL_GROUP_BY',''));

```




## Solution 1: Remove ONLY_FULL_GROUP_BY from mysql console

```
SET GLOBAL sql_mode=(SELECT REPLACE(@@sql_mode,'ONLY_FULL_GROUP_BY',''));
```

Be aware that this setting is NOT persistent across restarts, then use

```
SET PERSIST sql_mode=(SELECT REPLACE(@@sql_mode,'ONLY_FULL_GROUP_BY',''));
```


