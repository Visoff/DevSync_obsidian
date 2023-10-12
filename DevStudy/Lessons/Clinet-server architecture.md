There are a couple of ways you could think about client-server architecture. The most understandable one is like a dialog of client and server. But what would we change?

>It's simple REST api and here we go...

No, not really... Or so it depends. If you have real time app like game or workspace like figma/vscode, it's not ideal to limit yourself to REST apis.

>So, what's the difference and what should I choose then

It's very complicated and project depended, but generally, the more ways to do the same thing, the better. Because in the world of software engineering there are no solutions, only trade-offs. So let's get started by splitting all communication into 2 parts: Short lived and long lived connections

## Short lived connections
It's our REST api along with some tooling for that. Like graphql
What even is that? It's just a tool to get not only response with data, but also fetch response schema in advance. It's built on top of REST api, so it's just quality of life tool

## Long lived connections
Here it gets interesting. Let's imagine you have dynamically updating leaderboard. How would you approach this?
You might do something similar, to polling
Basically, it's where you send REST request to the server with some frequency and if there is something new response carries it to the client. But there are ways to create long lived tcp connection between client and server. This will allow server to send messages to client and update leader board with little to no delay
The most popular option is websocket connection. It's two way connection allowing for light messaging between client and server. To initiate it client first has to send request, and server has to "upgrade" the connection. After this it done, this request left us opened tcp connections, where we can exchange messages without the need for http headers and stuff.
Alternatively, you might think "oh, I don't send much data to the server, it's potential wasted". And trying to solve it we invented sse(server sent events), it's like websockets, but one sided, and not like REST, it allows browsers to long poll your server event, automatically update and ping connection. It supports multiple events, so you can open one sse, other then multiple ws.