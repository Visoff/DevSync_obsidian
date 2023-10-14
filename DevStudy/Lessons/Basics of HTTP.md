[[Text and media markup HTML]]HTTP is the protocol built on top of the TCP/IP //useless but interesting info
Example of HTTP protocol:
Get:
``` http
GET /user/info?user=you HTTP/1.1
Host: localhost:8080
User-Agent: Mozilla/5.0 ...
Accept: application/json

```
Others:
``` http
POST /user/data HTTP/1.1
Host: localhost:8080
Content-Type: application/json

{"user":"data", "friends":["none"]}
```

Let's break it down line by line:
1. At the first line we specify request goal, what it wants to do(endpoint)
	To do so we use 3 different parameters:
	- HTTP Verb (GET, POST, PATCH, PUT, DELETE, HEAD, OPTIONS, ...)
	- Uri
	- Http version
	Verb is used to specify action done with object represented with uri and this command is transfered by standarts of specified http version
2. Headers - a bunch of key-value paris most of which are automaticly generated
3. Body(not in GET) - free to use space to put any string formatted data

#SyncStudy