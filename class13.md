# what I learned 

* what the use sees :
![forms](https://twilio-cms-prod.s3.amazonaws.com/images/forms-header.width-808.png)

* what actually happens
![server](http://thenewcode.com/assets/images/client-server-2x.jpg)

## Forms
SENDING FORM DATA

### Form attributes:

* action = "url : the data will be sent to the specified url / if none to the same page.
* method = "GET" : the data will be sent as a request in the header. (url/?key=value&key2=value2).
* method = "POST" : the data will be sent as a request in the body. (more secure, better for lonfer data, and sending files).

### Form tag attributes:
* action = "/path-to-url"
* method = "GET/POST"
* name = "formName"
* autocomplete = "on/off"
* target = "_blank" (new tab) / "_self" (current tab)
* enctype = "text/plain" (text input form) "multipart/form-data" (forms containing files)


## What is the the difference between POST and GET?
, let’s step back and examine how HTTP works. Each time you want to reach a resource on the Web, the browser sends a request to a URL. What are the HTTP request consist?

- two parts:
1. a header that contains a set of global metadata about the browser’s capabilities.
2. body that can contain information necessary for the server to process the specific request.


### GET method:

* Uses
it used by the browser to ask the server.
send back a given resource.
The data is appended to the URL as a series of name/value pairs.
POST method:
It as simple as that :
“Hey server, take a look at this data and send me back an appropriate result.” If a form is sent using this method, the data is appended to the body of the HTTP request.