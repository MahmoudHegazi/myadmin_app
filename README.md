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

I solved a alot , a lot of problems to build that app with professional way and use ajax 


### last problem with chat
user must click on the friend to call ajax and get the messages if his friend send him message
or even the user we can't see it without reload. only noob solvent will make the app cry
repeate settimeout each second to check for the new messages




##### If you Wanna build one Like this visit udacity.com to learn how to become full stack web developer
