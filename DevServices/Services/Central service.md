To configure server which is using multiple services we can setup centeral service. It's done via json file.

Let's expose one service at some path
``` json
{
  "type":"proxy",
  "uri":"...",
  "service":"..."
}
```

But to make comunications between services we'll have to create an endpoint
``` json
{
  "type":"endpoint",
  "request":{/* proxy || request || chain logic */},
  "exposed":{
    "uri":"...",
    "port":80
  }
}
```
Here we expose some uri at some port to handle specific request

And now let's configure that endpoint to send request to specific service with specific data(uri, headers, body), keep in mind, that body and headers will merge
``` json
{
  "type":"request",
  "service":"...",
  "uri":"",
  "headers":{},
  "body":"..."
}
```

And now let's make an endpoint wich uses multiple services.
If service is depended on other service use chain
``` json
{
  "type":"chain",
  "from":{/* request logic */},
  "place":[
  {
    "from":["body", "path.to.value"],
    "into":["header", "key"]
  }
  ],
  "into":{/* request logic */}
}
```
And if requests are independent we can send them in parralel and then merge results
``` json
{
  "type":"merge",
  "requests":[]// request[]
}
```