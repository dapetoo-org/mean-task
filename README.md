
# MEAN Stack Implementation on AWS EC2 Instance

**MEAN (MongoDB, ExpressJS, AngularJS and NodeJS)**
MEAN is a collection of different Javascript technologies that enables faster application development. It is widely used by developers. The four technologies that made up of MEAN stack are all developed with JavaScript and this makes it much easier for developers with background in JavaScript to develop a full stack application with MEAN. 
MongoDB is a NoSQL database which is used to store application data in form of documents.
ExpressJS is a JavaScript framework for building server-side application
AngularJS is a JavaScript framework for building intuitive user interface and is mostly used for building single web page application.
NodeJS is a JavaScript runtime for executing JavaScript outside of the browser.

## Requirements
- AWS Account
- Ubuntu Server
- Terminal for SSH access to the EC2 Instance
- MongoDB installed on the EC2 Instance
- Nodejs and npm installed on the server

## Tech Stack

**Client:** AngularJS, HTML

**Server:** Node, Express

**Database:** MongoDB 

**Web Server:** EC2 Instance


## Lessons Learned

MEAN Stack implementation on AWS using Ubuntu 20.04 to create a simple Book application where the user can add the following details which will be saved in the database
- Name
- Author
- ISBN number
- Pages

## Challenges
I started the project with Ubuntu 22.04 and officially MongoDB is not currently supported on Ubuntu 22.04, I checked through the forum to find a workaround, but I tried everything and it still did not fix it. I had to downgrade the EC2 instnce to Ubuntu 20.04.



## Steps By Step
### Installing NodeJS
Make sure the packages required to run NodeJS and MongoDB are available are up to date
Install nodejs and npm

```
sudo apt update -y
sudo apt install nodejs npm -y
```

Confirm NodeJS and npm
```
node -v
npm -v
```

### Installing MongoDB

Install mongodb database by adding the key
Install mongodb
Start MongoDB
Enable MongoDB to start at startup
Check mongodb running status

```
sudo apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv 0C49F3730359A14518585931BC711F9BA15703C6
echo "deb [ arch=amd64 ] https://repo.mongodb.org/apt/ubuntu trusty/mongodb-org/3.4 multiverse" | sudo tee /etc/apt/sources.list.d/mongodb-org-3.4.list
sudo apt install -y mongodb
sudo service mongodb start
sudo systemctl enable mongodb
sudo systemctl status mongodb
```

### Project Initialization
Create a NodeJS application by running npm init and followed the prompt to initialize the Project and install Express and MongoDB package dependency for running a MEAN stack application and body-parser to process JSON request

#### Install all necessary package for our book application

```
npm install express 
npm install mongoose
npm install body-parser
```



## Demo/Running the application

Inside the project folder run the command below:

```
node server.js
```

Access the project on your web browser using **http://IP-ADDRESS:3000**

## Screenshots

![App Screenshot](https://via.placeholder.com/468x300?text=App+Screenshot+Here)

