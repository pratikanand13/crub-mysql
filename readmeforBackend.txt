Create a folder for backend
-> run npm init 
-> create a index.js file
-> in package.json add "scripts": {
    "start": "node src/index.js",
    "dev": "nodemon src/index.js"
  },
-> in index.js define express and define ports and from here we will manage all the different tasks to be execiuted mainly the crud app

now setup the MySQL 
download it from website also download workbench 
set it up
create a new db
connect to db
define a new schema 
now create schema with queries -> 
USE taskdb;

CREATE TABLE users (
    id INT AUTO_INCREMENT PRIMARY KEY,
    name VARCHAR(255) NOT NULL,
    email VARCHAR(255) UNIQUE NOT NULL,
    age INT,
    mobile VARCHAR(20),
    work VARCHAR(255),
    `add` VARCHAR(255), 
    description TEXT
);

INSERT INTO users (name, email, age, mobile, work, `add`, description) -- Fixed by using backticks
VALUES ('pratik', 'pratik@messi.com', 22, '1234567890', 'Developer', 'BIHAR', 'learner');

SELECT * FROM users;



now execute the command ( a pop up will come with following details

sql part is now dome
now we connect the databse to our node application
-> crearte a db folder
-> create conn.js
-> in conn.js first npm i mysql2
require it
create a conn function enter your details
use try catch to see successful connection

DB SUCCESSFULLY CONNECTED

now we come to crud part
create a routers folder 
define a crud.js
now in this 
npm i express
require it and all the diff things
now as we are told to use async function we refer to the documentation and create a queryAsync is used to convert the conn.query function, which is traditionally callback-based, into a Promise-based function

now we acquire our app

now we use crud 

done 