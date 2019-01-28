# mongoDB
mongoDB installation using ubuntu 16.04
How to create Admin user in mongoDB using following commands:--

db.createUser({	user: "admin", pwd: "admin", roles:[{role: "userAdminAnyDatabase" , db:"admin"}]})


