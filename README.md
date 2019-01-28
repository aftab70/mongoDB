# mongoDB
mongoDB installation using ubuntu 16.04
How to create Admin user in mongoDB using following commands:--

db.createUser({	user: "admin", pwd: "admin", roles:[{role: "userAdminAnyDatabase" , db:"admin"}]})

How to login using user or password by following the commands:--

mongo --port 27017 -u "admin" -p "admin" --authenticationDatabase "admin"


