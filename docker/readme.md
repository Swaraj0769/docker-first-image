sudo => super user do

apt => advance package tool

```
1. sudo apt update,
2. sudo apt upgrade, 
3. sudo apt install nodejs
4. sudo apt install npm
5. npm --version
6. node --version
```
pwd => to see the location of the file like /home/ubuntu

# second terminal ->
reset -> 1. scp [".pem key name"] [file name] [host-destination]our route
example:
    scp -i "hallex-test-1.pem" ./server.js ubuntu@ec2-15-207-247-178.ap-south-1.compute.am
azonaws.com:/home/ubuntu/express-project/server.js

# ubuntu terminal ->
1. pwd
2. ls => to see the existing files or directory
3. mkdir express-project => to create a new folder.
4. touch server.js => to create a new file.
5. cat server.js => to see the content of file like server.js

-> npm i
-> npx nodemon server.js
-> http://public-address:3000 => http://15.207.247.178:3000


# create a dockerfile:

``` 
FROM node:18 
#Linux OS + nodejs

WORKDIR /app

COPY package*.json ./   
#Copy package.json and package-lock.json to the working directory

RUN npm install

COPY server.js ./

EXPOSE 3000

CMD ["node", "server.js"]
```


# terminal :
```
docker build -t halley .
docker build -t halley file-path

to see a docker image : docker images in terminal
```