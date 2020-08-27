# myadmin_app
Final Version Work 

super not enogh (Get All messaage bettwen 2 users oder it bydate render it in super professional way

```sql
SELECT body FROM messages WHERE sender_id = 1 or sender_id=3 AND reciver_id = 1 or reciver_id =3;
```

```sql
SELECT body FROM messages WHERE sender_id = 1 or sender_id=3 AND reciver_id = 1 or reciver_id =3
ORDER BY sent_date ASC;
```

I realized that my SQL query will not return what I need It will return any message contains on of the two id
so my solvent was like this and this work 190%


```sql
SELECT body, sender_id, reciver_id FROM messages WHERE sender_id = 120 AND reciver_id= 3 
OR
sender_id = 3 AND reciver_id = 120 ORDER BY sent_date ASC;
```
