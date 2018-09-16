### Pre-requisites
Download and install the Brackets app from https://brackets.io. The Brackets app provides the live preview and autocomplation of HTML to make the learning of web programming easier and more intuitive.

* * *
[youtube https://youtu.be/vJ4x0-F-hLA]

* * *

### Basic format of HTML

HTML is like a tree with two big branches. The root of the tree is an `html` element. The `<html>` element has two child elements -- the `<head>` element and `<body>` element. An element starts by opening with `<` and closes with `</>`. For example, `<html>` tag is closed with `</html>`

```html
<!DOCTYPE html>
<html>
    <head>
        <title>Hello HTML</title>
    </head>
    <body>
        <h1>This is a header.</h1>
        <p>This is a pharagraph.</p>
    </body>
</html>
```

For practice, you can simplify the coding by ignoring `<!DOCTYPE html>` and the `head` element. The simplified version is shown below.

```html
<html>
    <body>
        <p>Some content...</p>
    </body>
</html>
```

* * *
### HTML elements

There are many HTML elements, but this page listed some of the most frequently used HTML elements below.

#### Header (H1 ~ H6)
The header elements are used for headers and important words. There are six header tags -- `<h1>` ~ `<h6>`. `<h1>` is the biggest, and `<h6>` is the smallest.

__HTML Code__
```html
<html>
<body>
    <h1>This is a test.</h1>
    <h2>This is a test.</h2>
    <h3>This is a test.</h3>
    <h4>This is a test.</h4>
    <h5>This is a test.</h5>
    <h6>This is a test.</h6>
</body>
</html>
```

__Output__

# This is a test.
## This is a test.
### This is a test.
#### This is a test.
##### This is a test.
###### This is a test.

* * *
#### Paragraph (P)
The `<p>` tag is used for paragraphs.
__HTML Code__

```html
<html>
<body>
    <p>This is a paragraph.</p>
</body>
</html>
```

__Output__

This is a paragraph.


* * *
#### Horizontal Rule (HR)
The `<hr />` tag creates a horizontal line.

__HTML Code__

```html
<html>
<body>
    <p>This is a paragraph.</p>
    <hr />
    <p>This is another paragraph.</p>
</body>
</html>
```

__Output__

This is a paragraph.

* * *

This is another paragraph.

* * *
#### Break (BR)
The `<br />` tag creates a line break. This tag can be handy when you need to create vertical space.

```html
<html>
<body>
    My name is: <br />
    James Bond
</body>
</html>
```


__Output__

My name is:
James Bond

* * *
#### Unordered List (UL)
The `<ul>` tag creates a list. Inside the `<ul>` tag, you use `<li>` tag to insert a list item.

```html
<html>
<body>
    <h5>My favorite books</h5>
    <ul>
         <li>Diary of Wimpy Kid</li>
         <li>Harry Potter</li>
         <li>The Hobbit</li>
    </ul>
</body>
</html>
```


__Output__
#### My favorite books
* Diary of Wimpy Kid
* Harry Potter
* The Hobbit

* * *
###### Image (IMG)
The `<img>` tag is used for inserting an image. Use `src` attribute to specifiy the location of an image.

```html
<html>
<body>
    <img src="cat.gif">
</body>
</html>
```

__Output__
<img src="https://d37rfi63g2olb3.cloudfront.net/wp-content/uploads/2018/02/07142523/sample.gif">

* * *
While we reviewed only small portion of HTML tags, don't worry a bit!. You can discover and get familiar with more HTML tags as you play with HTML.