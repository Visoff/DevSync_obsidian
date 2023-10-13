## What is CSS?

CSS (Cascading Style Sheets) is the code that styles web content. _CSS basics_ walks through what you need to get started. We'll answer questions like: How do I make text red? How do I make content display at a certain location in the (webpage) layout? How do I decorate my webpage with background images and colors?

Like HTML, CSS is not a programming language. It's not a markup language either. **CSS is a style sheet language.** CSS is what you use to selectively style HTML elements. For example, this CSS selects paragraph text, setting the color to red:

CSSCopy to Clipboard

```
p {
  color: red;
}
```

Let's try it out! Using a text editor, paste the three lines of CSS (above) into a new file. Save the file as `style.css` in a directory named `styles`.

To make the code work, we still need to apply this CSS (above) to your HTML document. Otherwise, the styling won't change the appearance of the HTML. (If you haven't been following our project, pause here to read Dealing with files and HTML basics).

1. Open your `index.html` file. Paste the following line in the head (between the [`<head>`](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/head) and `</head>` tags):
    
    HTMLCopy to Clipboard
    
    ```
    <link href="styles/style.css" rel="stylesheet" />
    ```
    
2. Save `index.html` and load it in your browser. Do you see the changes?


### Anatomy of a CSS ruleset

Let's dissect the CSS code for red paragraph text to understand how it works:
![[Pasted image 20231013140328.png]]The whole structure is called a **ruleset**. (The term _ruleset_ is often referred to as just _rule_.) Note the names of the individual parts:

#### Selector
This is the HTML element name at the start of the ruleset. It defines the element(s) to be styled (in this example, `<p>`  elements). To style a different element, change the selector.

#### Declaration

This is a single rule like `color: red;`. It specifies which of the element's **properties** you want to style.

#### Properties

These are ways in which you can style an HTML element. (In this example, `color` is a property of the `<p>` elements.) In CSS, you choose which properties you want to affect in the rule.

#### Property value

To the right of the property—after the colon—there is the **property value**. This chooses one out of many possible appearances for a given property. (For example, there are many `color` values in addition to `red`.)

Note the other important parts of the syntax:

- Apart from the selector, each ruleset must be wrapped in curly braces. (`{}`)
- Within each declaration, you must use a colon (`:`) to separate the property from its value or values.
- Within each ruleset, you must use a semicolon (`;`) to separate each declaration from the next one.

To modify multiple property values in one ruleset, write them separated by semicolons, like this:

CSSCopy to Clipboard

```
p {
  color: red;
  width: 500px;
  border: 1px solid black;
}
```

### Selecting multiple elements

You can also select multiple elements and apply a single ruleset to all of them. Separate multiple selectors by commas. For example:

CSSCopy to Clipboard

```
p,
li,
h1 {
  color: red;
}
```
### Different types of selectors

There are many different types of selectors. The examples above use **element selectors**, which select all elements of a given type. But we can make more specific selections as well. Here are some of the more common types of selectors:

|Selector name|What does it select|Example|
|---|---|---|
|Element selector (sometimes called a tag or type selector)|All HTML elements of the specified type.|`p`  <br>selects `<p>`|
|ID selector|The element on the page with the specified ID. On a given HTML page, each id value should be unique.|`#my-id`  <br>selects `<p id="my-id">` or `<a id="my-id">`|
|Class selector|The element(s) on the page with the specified class. Multiple instances of the same class can appear on a page.|`.my-class`  <br>selects `<p class="my-class">` and `<a class="my-class">`|
|Attribute selector|The element(s) on the page with the specified attribute.|`img[src]`  <br>selects `<img src="myimage.png">` but not `<img>`|
|Pseudo-class selector|The specified element(s), but only when in the specified state. (For example, when a cursor hovers over a link.)|`a:hover`  <br>selects `<a>`, but only when the mouse pointer is hovering over the link.|

## Fonts and text

Now that we've explored some CSS fundamentals, let's improve the appearance of the example by adding more rules and information to the `style.css` file.

1. Add the `<link>` element somewhere inside your `index.html`'s head (anywhere between the `<head>` and `</head>` tags). It looks something like this:
    
    HTMLCopy to Clipboard
    
    ```
    <link
      href="https://fonts.googleapis.com/css?family=Open+Sans"
      rel="stylesheet" />
    ```
    
    This code links your page to a style sheet that loads the Open Sans font family with your webpage.
2. Next, delete the existing rule you have in your `style.css` file. It was a good test, but let's not continue with lots of red text.
3. Add the following lines (shown below), replacing the `font-family` assignment with your `font-family` selection. The property `font-family` refers to the font(s) you want to use for text. This rule defines a global base font and font size for the whole page. Since `<html>` is the parent element of the whole page, all elements inside it inherit the same `font-size` and `font-family`.
    
    CSSCopy to Clipboard
    
    ```
    html {
      font-size: 10px; /* px means "pixels": the base font size is now 10 pixels high */
      font-family: "Open Sans", sans-serif; /* this should be the rest of the output you got from Google Fonts */
    }
    ```

4. Now let's set font sizes for elements that will have text inside the HTML body(`<p>` `<h1>`, `<li>`). We'll also center the heading. Finally, let's expand the second ruleset (below) with settings for line height and letter spacing to make body content more readable.
    
    CSSCopy to Clipboard
    
    ```
    h1 {
      font-size: 60px;
      text-align: center;
    }
    
    p,
    li {
      font-size: 16px;
      line-height: 2;
      letter-spacing: 1px;
    }
    ```

Well, now you are ready to do it yourself!

CSS documentation (for searching styles):
```
https://developer.mozilla.org/en-US/docs/Web/CSS 
```

CSS tasks:
``` 
https://www.w3schools.com/css/css_exercises.asp
```

HTML and CSS:
``` 
https://cs396-web-dev.github.io/winter2022/assignments/lab01#:~:text=HTML%20files%20are%20for%20presenting,setting%20a%20various%20style%20properties 
```
