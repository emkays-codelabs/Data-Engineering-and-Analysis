

```
Catalog → Schema → Table
```

---

# 🟢 1️⃣ CATALOG COMMANDS

| Operation            | Command                              |
| -------------------- | ------------------------------------ |
| Show catalogs        | `SHOW CATALOGS;`                     |
| Create catalog       | `CREATE CATALOG demo_catalog;`       |
| Use catalog          | `USE CATALOG demo_catalog;`          |
| Describe catalog     | `DESCRIBE CATALOG demo_catalog;`     |
| Drop catalog         | `DROP CATALOG demo_catalog;`         |
| Drop catalog (force) | `DROP CATALOG demo_catalog CASCADE;` |

---

# 🔵 2️⃣ SCHEMA (DATABASE) COMMANDS

| Operation           | Command                                         |
| ------------------- | ----------------------------------------------- |
| Show schemas        | `SHOW SCHEMAS IN demo_catalog;`                 |
| Create schema       | `CREATE SCHEMA demo_catalog.demo_schema;`       |
| Use schema          | `USE demo_schema;`                              |
| Describe schema     | `DESCRIBE SCHEMA demo_catalog.demo_schema;`     |
| Drop schema         | `DROP SCHEMA demo_catalog.demo_schema;`         |
| Drop schema (force) | `DROP SCHEMA demo_catalog.demo_schema CASCADE;` |

---

# 🟡 3️⃣ TABLE COMMANDS

| Operation                | Command                                                                                                |
| ------------------------ | ------------------------------------------------------------------------------------------------------ |
| Show tables              | `SHOW TABLES IN demo_catalog.demo_schema;`                                                             |
| Create table             | `CREATE TABLE demo_catalog.demo_schema.customers (id INT, name STRING);`                               |
| Create table from select | `CREATE TABLE demo_catalog.demo_schema.new_table AS SELECT * FROM demo_catalog.demo_schema.customers;` |
| Describe table           | `DESCRIBE TABLE demo_catalog.demo_schema.customers;`                                                   |
| Insert data              | `INSERT INTO demo_catalog.demo_schema.customers VALUES (1,'Mahesh');`                                  |
| Select data              | `SELECT * FROM demo_catalog.demo_schema.customers;`                                                    |
| Update data              | `UPDATE demo_catalog.demo_schema.customers SET name='Kumar' WHERE id=1;`                               |
| Delete rows              | `DELETE FROM demo_catalog.demo_schema.customers WHERE id=1;`                                           |
| Delete all rows          | `TRUNCATE TABLE demo_catalog.demo_schema.customers;`                                                   |
| Add column               | `ALTER TABLE demo_catalog.demo_schema.customers ADD COLUMN age INT;`                                   |
| Drop column              | `ALTER TABLE demo_catalog.demo_schema.customers DROP COLUMN age;`                                      |
| Rename table             | `ALTER TABLE demo_catalog.demo_schema.customers RENAME TO demo_catalog.demo_schema.clients;`           |
| Drop table               | `DROP TABLE demo_catalog.demo_schema.clients;`                                                         |

---

# 🟣 4️⃣ VIEW COMMANDS

| Operation   | Command                                                                                                      |
| ----------- | ------------------------------------------------------------------------------------------------------------ |
| Create view | `CREATE VIEW demo_catalog.demo_schema.customer_view AS SELECT name FROM demo_catalog.demo_schema.customers;` |
| Show views  | `SHOW VIEWS IN demo_catalog.demo_schema;`                                                                    |
| Drop view   | `DROP VIEW demo_catalog.demo_schema.customer_view;`                                                          |

---

# 🟤 5️⃣ PERMISSION COMMANDS

| Operation         | Command                                                                              |
| ----------------- | ------------------------------------------------------------------------------------ |
| Grant permission  | `GRANT SELECT ON TABLE demo_catalog.demo_schema.customers TO 'user@example.com';`    |
| Revoke permission | `REVOKE SELECT ON TABLE demo_catalog.demo_schema.customers FROM 'user@example.com';` |
| Show grants       | `SHOW GRANTS ON TABLE demo_catalog.demo_schema.customers;`                           |

---

# ⚫ 6️⃣ CONTEXT COMMANDS

| Operation       | Command                     |
| --------------- | --------------------------- |
| Current catalog | `SELECT current_catalog();` |
| Current schema  | `SELECT current_schema();`  |

---

# 🔴 CASCADE SUMMARY

| Object  | Normal Drop                  | Force Drop                           |
| ------- | ---------------------------- | ------------------------------------ |
| Table   | `DROP TABLE table_name;`     | —                                    |
| Schema  | `DROP SCHEMA schema_name;`   | `DROP SCHEMA schema_name CASCADE;`   |
| Catalog | `DROP CATALOG catalog_name;` | `DROP CATALOG catalog_name CASCADE;` |

---

