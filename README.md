# nitemswapping
The project is about " N item Swapping" which means , anyone can use the portal and do swapping of items. This is a course based project and currently in progress. 

#Please follow the below steps to make it work in your local machine

Step 1 : Install command line mongo database and try to run it using below similar commands.
Once you have installed the mongo database, please try to run using below similar commands.

Terminal 1 : mongod --dbpath "c:\UNCC\NBAD\mongodb\data\db"

Terminal 2 : mongo.exe

Here, terminals are windows terminal. If \data\db folders do not exists, please make sure you create those.

Step 2 : Populate the database.
Once you have completed the step 1, make sure you run the commands provided in the file namely " populateDatabaseScript.txt "

Step 3 : Once you are all set with above steps, you can go to /public/ folder and execute below command.

>> nodemon app.js

OR

>>node app.js

Note : Running using nodemon is option as its easier way to keep the app run always.

Issues and its fix : 

You may come across below like errors,So please fix them as per mentioned solution.

1. Error

C:\UNCC\NBAD\Assignments\Final Project\public>nodemon app.js
[nodemon] 1.18.4
[nodemon] to restart at any time, enter `rs`
[nodemon] watching: *.*
[nodemon] starting `node app.js`
internal/modules/cjs/loader.js:583
    throw err;
    ^

Error: Cannot find module 'mongoose'
    at Function.Module._resolveFilename (internal/modules/cj
    
Solution: 

C:\UNCC\NBAD\Assignments\Final Project\public>npm install mongoose --save
npm WARN public@1.0.0 No repository field.

+ mongoose@5.4.3
added 91 packages from 78 contributors and audited 212 packages in 5.023s
found 0 vulnerabilities

Do same for all similar kind of errors

2. Error

C:\UNCC\NBAD\Assignments\Final Project\public>nodemon app.js
[nodemon] 1.18.4
[nodemon] to restart at any time, enter `rs`
[nodemon] watching: *.*
[nodemon] starting `node app.js`
connection error: { MongoNetworkError: failed to connect to server [localhost:27017] on first connect [MongoNetworkError: connect ECONNREFUSED 127.0.0.1:27017]
    at Pool.<anonymous> (C:\UNCC\NBAD\Assignments\Final Project\public\node_modules\mongodb-core\lib\topologies\server.js:564:11)
    at Pool.emit (events.js:182:13)
    at Connection.<anonymous> (C:\UNCC\NBAD\Assignments\Final Project\public\node_modules\mongodb-core\lib\connection\pool.js:317:12)
    at Object.onceWrapper (events.js:273:13)
    at Connection.emit (events.js:182:13)
    at Socket.<anonymous> (C:\UNCC\NBAD\Assignments\Final Project\public\node_modules\mongodb-core\lib\connection\connection.js:246:50)
    at Object.onceWrapper (events.js:273:13)
    at Socket.emit (events.js:182:13)
    at emitErrorNT (internal/streams/destroy.js:82:8)
    at emitErrorAndCloseNT (internal/streams/destroy.js:50:3)
  
Solution : You don;t have the mongo db running properly. Please make sure the database setup is working correctly.

