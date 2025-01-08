---
Theme: "[[Database]]"
---
Информации о колонках:

```sql
SELECT
	column_name,
	data_type,
	character_maximum_length,
	is_nullable
FROM
	information_schema.columns;
```

Проверка индексов:

```sql
SELECT
	indexname,
	indexdef
FROM
	pg_indexes
WHERE
	tablename = 'table';
```

Размер таблицы:

```sql
SELECT
	pg_size_pretty(pg_total_relation_size('table')) AS total_size;
```

Статистика по количеству строк в таблицах текущей схемы:

```sql
SELECT
	relname AS table_name,
	n_live_tup AS row_count
FROM
	pg_stat_user_tables
ORDER BY
	row_count DESC;
```