Javascript is memory save, garbage collected, interpreted or just in time compiled programming language, designed specifically for building interactive websites.
But nowdays to powers a lot more than just websites. Powerful backends and so much more heart taking frontend experiences could be build with Javascript.
Let's dive in with some quick examples

First of all, to run javascript you can use your browser or specific runtime environment(we'll talk about those later). In your browser click f12 to open developer tools, there is console, which takes javascript code and initializes it line by line

Let's create variable. There are 3 ways to create variable, now we'll talk about 2 of them: const and let.
With let we create mutable variables:
``` js
var a = 1
a = 2
a// 2
```
And with const we create immutable variables:
``` js
const a = 1
a = 2// Uncaught TypeError: Assignment to constant variable.
a// 1
```

We can do basic math calculations with variables
``` js
let a = 1
a+1// 2
a-1// 0
a+=1
a++
a// 3
a*3// 9
a%2// 1
```

Now let's move to any folder and create index.html file
``` html
<html>
	<head>
		<script src="./index.js"></script>
	</head>
</html>
```
And create index.js file, it will be the place we write our javascript.
Open index.html to initialize javascript

We can also enclose this logic in functions
``` js
function f(x) {
	return x**2
}

let q = (x) => {
	return x**2
}

// f(x) = q(x) - square function
f(3)// 9
q(4)// 16
```
There are some built in functions like these:
``` js
console.log("anything")// outputs data in console == print
Math.sin(Math.PI)
Math.cos(Math.PI)
```

We can clean repeating code with loops
``` js
let i = 0
while (i < 10) {
	i++
}

// equivalent

for (let i = 0; i < 10; i++) {
	// do something 10 times
}
```

#SyncStudy