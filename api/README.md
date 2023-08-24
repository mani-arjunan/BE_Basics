# API

APIs are the one that enables communication between two software components, basically two computers talk together using
api's to exchange data or get information or to perform some functionalities etc.

## There are multiple type of apis``

- Soap API
  `SOAP api are used in past, where the computers exchange messages in the format of XML.`
- RPC API
- REST API
  `REST is the most popular and widely used api protocol, where the client sends a request to server and the server responds with the data, usually the data can be in the format of JSON, recent days Proto_buffer format data is also possible.`
- Websocket API
  `It supports two way communication where the server sends callback to the client and the client can sneak server events to support real time communication.`

## HATEOAS

Hypermedia As The Engine Of Application State, => means basically links hypermedia links will return as a response, where those links provides another website or apis also.

## Authentication

The api authentication is an important step whenever any api's are created, This ensures that the client attempting to request the resource should have a valid access, in simple terms not all can access any api's, this ensures security.

Usually there are two parts in this

- Authentication - Authentication is basically login, signup etc.
- Authorization - Authorization specifies whether the requester has the access to the api or not.

Below is the list of ways of authenticating an api

- username and password authentication
- Biometric authentication like FaceId, TouchId etc
- Email authentication
- SSO login, eg: one single google login for gmail, gmeet, drive, google photos, google docs etc, without sso we would have end up logging into each service with different ids and passwords.

Below is the list of ways for authorizing an api

- OAuth - Open protocol for authorization that allows users to share their data to third party, eg: any google login in random websites, where once logged in via google, that random websites can have that user google data.
- JWT - Jason Web Token is used for authorization, for eg: when a user login a website using username and password, the server sends a JWT token along with it, client stores that token for the subsequent request where the server verifies that jwt token and responds to that request.

   JWT's three important components

   - Header: Define token type and the signature algorithm involved eg: RS256, HS256 etc.
   - Payload: Requestor body.
   - Signature: secure key.

  How JWT are created?

  - There are multiple algorithms to create a JWT token like RS256, HS256 etc.
  - basically combines base64 of payload, header and secret key from server and creates a token.
  - when the token comes, it verifies by decoding the token and comparing it with the secret key, if matches you are good to go.

- Token - Token based authorization is one of the most used, it basically generates a token when a client login with username and password, but unlike JWT this time server stores that token in db or some redis cache and revalidates the subsequent client request with the same token.
- Session - Session based authorization is similar to token based, instead it generates a random id and sends it to client, the client stores in the cookie, and for the subsequent request server reads the client cookie and validates.
- Basic auth - It is the basic authorization where the username and password is send to each request.

## REST API
    REST(Representational State Transfer) one of the most popular API methods.

- REST is stateless, meaning the server does not need to know about the client and vice versa.
- In REST the client sends request to server to reterive, modify or insert resources.
- Usally REST api should follow the below protocol
    - http verb must be sent eg: GET, POST, PATCH etc.
    - request headers must be sent, which contains some information about the requestor. 
    - a path to the resource, eg endpoint /get-users, /set-users, /login, /signup etc.
    - payload, it is the data that needs to be updated or inserted in to the server.

## Graphql
- Graphql is an updation of REST where only POST method is supported, in this single method update, insert, get all are possible, one advantage of using graphql is its like a query based API method where we can only query certain neccesary fields that the client  is needed.

## GRPC(TODO)
GRPC stands for remote procedure call, it is the modern open source RPC framework, it supports both request response type of connection as well as  long running stream connection

