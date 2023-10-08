Javascript is interpreted or just in time compiled language, which means that there are some algorithms called compilers that run javascript. The most popular one is V8 engine. It is inside of chrome browser and Node js.

What is Node and why should I use it?
Node is the place to run javascript, it's not a language, framework or library.
You should use runtime like node to run javascript as an app(for backend) or easy acess to libraries via npm.

First of all download and install node
To check if it installed correctly you can run
``` bash
node --version
```
With standart node distribution you usually install node package manager(npm)
Check that it is also installed
``` bash
npm --version
```

Now create empty folder and run this inside
``` bash
npm init -y
```
This will create package.json file for configuring your project

Now create index.js file
``` js
console.log("hello in node")
```

You can run your whole project by using
``` bash
npm run
``` 
or you can run independed files with
``` bash
node index.js
```

#SyncStudy