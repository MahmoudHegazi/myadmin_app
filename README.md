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

Possible it not only possbile i going to work:
https://www.cloudways.com/blog/real-time-php-notification-system/

## not working yet


```php
<?php

//  Call this function when data changes
function update_clients()
{
    mysql_query( "UPDATE pageGen SET id = id + 1 LIMIT 1" );
}

//  Call this function to get the ID to pass to JavaScript
function get_update()
{
    $result = mysql_query( "SELECT id FROM pageGen LIMIT 1" );
    $update = mysql_result( $result, 0, 'id' );
    return $update;
}

?>
When the page is initially loaded, populate a JavaScript variable with a number from the database:

<script type="text/javascript">
var pageGenID = 25218603  //  generated by PHP
var processUpdate = function( response ) 
{
    if ( pageGenID < response ) 
    {
        replace_current_data_with_new_via_ajax();
        pageGenID = response;
    }
}
//  Compare our Page Generate ID against that of the server
var checkUpdates = function()
{
    serverPoll = setInterval( function()
    {
        $.get('script_to_return_latest_pageGenID.php', 
          { lastupdate: 1 }, 
          processUpdate, 'html');
    }, 10000 )
};

//  Check for updates every 10 seconds
$( document ).ready( checkUpdates );

</script>


```
https://stackoverflow.com/questions/4629642/how-can-i-refresh-a-page-when-a-database-is-updated


##### If you Wanna build one Like this visit udacity.com to learn how to become full stack web developer
