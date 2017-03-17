Zally WEB-UI
============

Zally Web-UI project provide a web user interface to lint your api specs.
Proudly build with NodeJS and React.

## Requirements

* NodeJS >= 6.0.0


## Install and Run

```bash
cd web-ui
npm install --production
npm start
```

## Configuration

The web-ui rely on [dotenv](https://github.com/motdotla/dotenv) NodeJS module to handle configuration.
Following the [The Twelve-Factor App](https://12factor.net/config) methodology.
Customization can be done by setting environment variables and/or by providing a `.env` file in the web-ui root directory.<br>

Below the full reference of "available" environment variables and their default values.

```
PORT=8442
LOG_LEVEL="debug"
SSL_ENABLED=false
SSL_CERT_DIR="cert"
OAUTH_ENABLED=false
OAUTH_CLIENT_ID=""
OAUTH_AUTHORIZATION_URL=""
OAUTH_REDIRECT_URI=""
OAUTH_TOKENINFO_URL=""
OAUTH_SCOPES=""
ZALLY_API_URL=""
```

* **PORT**: HTTP(S) Server port
* **LOG_LEVEL**: Logging level (error|warn|info|verbose|debug|silly)
* **SSL_ENABLED**: Start the server with HTTPS 
* **SSL_CERT_DIR**: Directory where ```server.key``` and ```server.crt``` files are located
* **OAUTH_ENABLED**: Enable client side OAuth2 implicit grant flow protection
* **OAUTH_CLIENT_ID**: OAuth2 client id assigned to your app
* **OAUTH_REDIRECT_URI**: The route that should handle the OAuth2 access token response
* **OAUTH_TOKENINFO_URL**: The url used to validate the access token and retrieve token information
* **OAUTH_SCOPES**: Comma separated list of scopes that the user should grant to the app
* **ZALLY_API_URL**: The URL pointing to Zally Api Server


## Development

### Install

```
cd web-ui
npm install
```

### Run in development mode

```
npm run dev
```

> This task start the server in development mode with **nodemon** and **webpack-dev-server-middleware** watching for changes.


### Build optimized client javascript bundle

```
npm run build
```

### Build docker image

```
npm run docker:build
```
