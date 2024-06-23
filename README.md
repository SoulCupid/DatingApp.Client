# DatingApp.Client
Base work developed as part of this [course](https://www.udemy.com/course/build-an-app-with-aspnet-core-and-angular-from-scratch/).

### Create local certificates

The local certificates will help us run our Angular client app with https.

On the client folder root, create an ssl folder, place yourself there and run the following commands:

- mkcert -install
- mkcert localhost

Then we need to add this to your angular.json file, under serve:
```json
"options": {
            "ssl": true,
            "sslKey": "./ssl/localhost-key.pem",
            "sslCert": "./ssl/localhost.pem"
          }
```


### Run the app

There are two main ways to run the app. Please position yourself inside the _client_ folder.

The first is to run the application "normally" with the command:

`npm run start`

The second one is to run the app via Docker, with the command:
`docker compose up -d`

Access the application in: `http://localhost:4200/`