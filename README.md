# [Swing Music](https://github.com/swingmx/swingmusic)  Internal Api Docs
### note: this documentation is a work in progress
### endpoint info
All api endpoints are as far as I can tell, just paths off of the main instance. (eg. `https://localhost:1970/endpoint here`)
## Authorization
Authorization is provided through the `Cookie` header in requests to the api.<br>
The header should look something like this: `access_token_cookie=a bunch of letters and stuff`
### login
#### endpoint
`/auth/login`
#### method
POST
#### request
JSON data with the following structure
`{"username":"USERNAME HERE","password":"PASSWORD HERE"}`
#### response
The server should respond with the `Set-Cookie` header, which is the authorization cookie.
