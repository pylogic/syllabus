# Training 3: internet data accessing

ganben

## Objectives

- HTTP protocols
- API access
- weibo APIs

## HTTP protocols

HTTP = '[Hypertext Transfer Protocal](https://www.w3.org/Protocols/)', is a short connected protocol. you should know some [important concept](https://www.tutorialspoint.com/http/index.htm):

- HTTP is connectionless, media independent and stateless,
- HTTP version, format and URI and content parameters,
- HTTP message's request/response and it's headers,
- Request method/parameters
- Response code/parameters
- Authorization and Cookie
- Cache controls
- URL encodings

## how API works

[RESTful](https://www.tutorialspoint.com/restful/index.htm) Web Services: is short for 'Representational state transfer'. you should understand:

- RESTful operations
- URI rules and route principle
- python restful frameworks : [flask](http://flask.pocoo.org/)
- and its [dispatching implementation](http://flask.pocoo.org/docs/0.12/quickstart/#routing)
- Endpoints and replied data generation

## Weibo API

you are going to learn how to read [API documents](http://open.weibo.com/wiki/%E9%A6%96%E9%A1%B5) and verifys its features.

read an example of [agongdai](https://github.com/agongdai/weibo-api) understand:

- what's App key and secret and how to get it
- what's access token and how to get it
- who is call this function from where for what? 
- what is the URI path for a specific user's newest post?
- how many features are supported by weibo API document?

## Tasks

- Find http message examples of HTTPS transfer a jpeg file with cookies, HTTP post a form data and response a HTML, HTTP GET with URI parameter and response with file, HTTP post JSON data with token and response with XML
- use python lib requests to execute GET/POST to baidu, sina, and douban and record the response
- run a flask project to provide two API with following rules: rootpath/findpostbyusername/?username/?blogid   rootpath/findpostbydate/?date/?pagesize and reply a JSON list data(mocked)
- write a weibo crawler of updating newset posts every 10 seconds and print it out