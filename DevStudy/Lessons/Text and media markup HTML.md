### What are Tags and Attributes?
Tags and attributes are the basis of HTML.

They work together but perform different functions – it is worth investing 2 minutes in differentiating the two.

### What Are HTML Tags?
Tags are used to mark up the start of an HTML element and they are usually enclosed in angle brackets. An example of a tag is: <h1>.

Most tags must be opened <h1> and closed </h1> in order to function.

### What are HTML Attributes
Attributes contain additional pieces of information. Attributes take the form of an opening tag and additional info is placed inside.

An example of an attribute is:

```
<img src="mydog.jpg" alt="A photo of my dog.">
```

In this instance, the image source (src) and the alt text (alt) are attributes of the <img> tag.

Golden Rules To Remember
The vast majority of tags must be opened (<tag>) and closed (</tag>) with the element information such as a title or text resting between the tags.
When using multiple tags, the tags must be closed in the order in which they were opened. For example:

```
<strong><em>This is really important!</em></strong>
```

## Creating Your First HTML Webpage
First off, you need to open your HTML editor, where you will find a clean white page on which to write your code.

From there you need to layout your page with the following tags.

### Basic Construction of an HTML Page
These tags should be placed underneath each other at the top of every HTML page that you create.

<!DOCTYPE html> — This tag specifies the language you will write on the page. In this case, the language is HTML 5.

<html> — This tag signals that from here on we are going to write in HTML code.

<head> — This is where all the metadata for the page goes — stuff mostly meant for search engines and other computer programs.

<body> — This is where the content of the page goes.

### Further Tags
Inside the <head> tag, there is one tag that is always included: <title>, but there are others that are just as important:

<title>
This is where we insert the page name as it will appear at the top of the browser window or tab.
<meta>
This is where information about the document is stored: character encoding, name (page context), description.
Let’s try out a basic <head> section:

```
<head>
<title>My First Webpage</title>
<meta charset="UTF-8">
<meta name="description" content="This field contains information about your page. It is usually around two sentences long.">.
<meta name="author" content="Conor Sheils">
</header>
```

### Adding Content
Next, we will make <body> tag.

The HTML <body> is where we add the content which is designed for viewing by human eyes.

This includes text, images, tables, forms and everything else that we see on the internet each day.

### How to Add HTML Headings To Your Web Page
In HTML, headings are written in the following elements:

<h1>
<h2>
<h3>
<h4>
<h5>
<h6>
As you might have guessed <h1> and <h2> should be used for the most important titles, while the remaining tags should be used for sub-headings and less important text.

Search engine bots use this order when deciphering which information is most important on a page.

#### Creating Your Heading
Let’s try it out. On a new line in the HTML editor, type:

```
<h1>Welcome to My Page</h1>
```

And hit save. We will save this file as “index.html” in a new folder called “my webpage.”

Well let’s not get carried away; we’ve still got loads of great features that we can add to your page.

### How To Add Text In HTML
Adding text to our HTML page is simple using an element opened with the tag <p> which creates a new paragraph. We place all of our regular text inside the element <p>.

When we write text in HTML, we also have a number of other elements we can use to control the text or make it appear in a certain way.

### Other Key Elements
They are as follows:

<b>	- Bold	Highlight - important information
<strong>	 - Strong	- Similarly to bold, to highlight key text
<i> - Italic - To denote text
<em> - Emphasised Text - Usually used as image captions
<mark> - Marked Text - Highlight the background of the text
<small>	Small Text	To shrink the text
<strike>	Striked Out Text	To place a horizontal line across the text
<u>	Underlined Text	Used for links or text highlights
<ins>	Inserted Text	Displayed with an underline to show an inserted text
<sub>	Subscript Text	Typographical stylistic choice
<sup>	Superscript Text	Another typographical presentation style

### File paths
To make files talk to one another, you have to provide a file path between them — basically a route, so one file knows where another one is. To demonstrate this, we will insert a little bit of HTML into our `index.html` file, and make it display the image you chose in the article "What will your website look like?" Alternatively, you can choose an existing image at your disposal, on your computer or from the Web, and use it in the following steps:

1. Copy the image you chose earlier into your `images` folder.
2. Open up your `index.html` file, and insert the following code into the file exactly as shown. Don't worry about what it all means for now — we'll look at the structures in more detail later in the series.

   HTMLCopy to Clipboard

    ```
    <!doctype html>
    <html lang="en-US">
      <head>
        <meta charset="utf-8" />
        <meta name="viewport" content="width=device-width" />
        <title>My test page</title>
      </head>
      <body>
        <img src="" alt="My test image" />
      </body>
    </html>
    ```

3. The line `<img src="" alt="My test image">` is the HTML code that inserts an image into the page. We need to tell the HTML where the image is. The image is inside the _images_ directory, which is in the same directory as `index.html`. To walk down the file structure from `index.html` to our image, the file path we'd need is `images/your-image-filename`. For example, our image is called `firefox-icon.png`, so the file path is `images/firefox-icon.png`.
4. Insert the file path into your HTML code between the double quote marks of the `src=""` code.
5. Change the contents of the `alt` attribute to a description of the image you are including. In this case, `alt="Firefox logo: flaming fox wrapping the world"`.
6. Save your HTML file, then load it in your web browser (double-click the file). You should see your new webpage displaying your image!