# ccashfrontend
This is a Front End for EntireTwix's CCcash API, it allows regular users to access the banks features and do what they like without having to know code or http requests.

## Deployment
To begin you must have set up CCash API server which you can find here [Github](https://github.com/EntireTwix/CCash) He is much better at documentation than i, but his is also harder to set up so good luck.

From here is will assume you have set up the api server, know its URL and what protocol it is using

if deploying to a serverless application make sure you set the environmental variables first. these are as follows
* BANKAPIURL=your api url including http/s and the trailing slash NOT BANKF
* SECURE=true if you have ssl on your front end host
* MONGO=put your mongodb url here (not required)
* MARKETPLACE=True if you want a market place, its not very good and not complete so i dont suggest using it. blank if not wanted
* SETUP=true when you have set the above this just gets rid of the setup page that will show if it equals false or the .env file is not found
* PORT=Optional will default to 3000 if not set

if you are deploying on a vps then
1. git clone repository
2. run npm install
3. run with your favourite node webserver if you dont know any use [pm2](https://pm2.keymetrics.io/)
4. go to localhost or the ip of the server
5. restart the application and badda bim badda boom you done

If you want to properly deploy it put it behind a reverse proxy too so you can have virtual hosts and all that shizzaz
but im not going to outline that because that is more advanced, and will require a lot of explaining, google `how to reverse proxy a nodejs app` if you want to know more
