# mongoDB
mongoDB installation using ubuntu 16.04


How to create Admin user in mongoDB using following commands:--

db.createUser({	user: "admin", pwd: "admin", roles:[{role: "userAdminAnyDatabase" , db:"admin"}]})

How to enable user authentication with mongoDB by following to add given lines in vim /etc/mongodb.conf

----------------------------------------------------------
security:
    authorization: enabled
setParameter:
   enableLocalhostAuthBypass: false

------------------------------------------------------------

How to login using user or password by following the commands:--

----------------------------------------------------------------------------------
mongo --port 27017 -u "admin" -p "admin" --authenticationDatabase "admin"
----------------------------------------------------------------------------------

or alternate method to verify username and password simply login mongodb to type mongo
on terminal 

---------------------------------------------------------------
mongo

use admin
switched to db admin
> db.auth("username", "password")

----------------------------------------------------------------
To delete user in mongoDB

Commands is 
db.dropUser("username");


use aftab
db.runCommand({ 
    "createUser" : "user", 
    "pwd" : "123456", 
    "customData" : {

    }, 
    "roles" : [
        {
            "role" : "dbAdmin", 
            "db" : "aftab"
        }
    ]
});


--------------------------------------------------------------------

How to create normal user in mongoDB

------------------------------------------------------------------------------
db.createUser(
   {
     user: "username",
     pwd: "password",
     roles: [ "readWrite", "dbAdmin" ]
   }
)

--------------------------------------------------------------------------------


use aftab
db.runCommand({ 
    "createUser" : "user", 
    "pwd" : "123456", 
    "customData" : {

    }, 
    "roles" : [
        {
            "role" : "dbAdmin", 
            "db" : "aftab"
        }
    ]
});
