# 100 - The Anatomy of a p5js Sketch

Based on "The Anatomy of a p5js Sketch" at https://openprocessing.org/sketch/1142253/

## 100 - A tutorial for new coders

Welcome to the wonderful world of p5js, where you can use simple Javascript code to create all manner of beautiful art, interactive apps, and fascinating graphics (not to mention playing sounds, using video from webcams, and reading inputs from sensors like accelerometers).

This tutorial will take you through the lines of code that make up a simple p5js sketch one by one, no Javascript experience needed.

## 200 - Code Comments

The first piece of code you need to know about, doesn't actually do anything at all: comments.

Comments come in two varieties:

- Single Line
- Multi-line

```
// This is a single line comment

/*
This is a multi-line comment
*/
```

Single line comments start with two forward slashes. Anywhere there are two forward slashes right next to each other, all of the rest of the text on that line will be ignored.

Multi-line comments start with a forward slash followed immediately by an asterisk (a.k.a. star character). As it's name implies a multi-line comment can by spread out over multiple lines, and it doesn't end until there is another asterisk **followed** by a forward slash. (Note: multi line comments can also be used on a single line, with the advantage that more code can come after the end of the comment.

Comments don't **do** anything when a sketch runs, but they are useful for explaining what the code around them is doing, and you'll see a lot of them in this tutorial.

## 300 - The setup Function

Every p5js sketch needs a **setup** function. But what is a function, you might ask? A function is a way to group together a series of javascript statements and give them a name. You can create your own functions that you will call later, which is a convenient way to reuse the same lines of code without typing them repeatedly in different places. But in the case of the **setup** function, this is a specially named function that p5js will call for us when the sketch first starts.

```
// This function will automatically be called once
// when we run our sketch
function setup() {
	// Our setup code will go here.
}
```

A function in javascript is made of the following parts:

- The **function** keyword
 
- The name of the function (must start with a letter, and contain only letters, numbers, and underscores).
 
- A list of parameters enclosed in parentheses
- - We'll cover parameters in more detail later.
- - The parentheses are required even if there are no parameters.

- The body of the function

- - Starts with an open curly brace {
- - Followed by a series of statements.
- - These statements will be executed each time the function is called.
- - Ends with a closing curly brace }

The most important thing that happens in the setup function is the creation of our canvas, which is where our graphics will be displayed. To do this we call the p5js **createCanvas** function.

```
// This function will automatically be called once
// when we run our sketch
function setup() {
	createCanvas(400, 400);
}
```

To call a function in javascript you simply use that function's name followed by an open parenthesis, a list of values to pass to the function (i.e. parameters), and a closing parenthesis. At the end of the line it is good practice to add a semi colon.

The **createCanvas** function takes two parameters*: the width of the canvas, and the height of the canvas. For starters we will create a canvas that is 400 pixels square. You can find documentation of the createCanvas function and all of the functions provided by p5js on [the p5js.org reference site](https://p5js.org/reference/#/p5/createCanvas).

* *technically createCanvas also takes a third optional parameter, a constant which specifies the type of renderer (two dimensional graphics: P2D, or  three dimensional graphics: WEBGL).*

## 400 - Filling the Canvas with a Color

Currently our sketch is pretty boring, it's just a plain white canvas on a plain white page (pretty much invisible). Let's make it visible by filling it with a single solid color.

The [background](https://p5js.org/reference/#/p5/background) function will fill the canvas with a color. There are several ways to specify what color to use.

```
// This function will automatically be called once
// when we run our sketch
function setup() {
	createCanvas(400, 400);
	// Let's make our canvas light blue
	background('LightBlue');
}
```

### 100 - Named Colors

Certain colors can be specified using a text value that specified the name of the color. A text value in javascript, also called a string, is a series of characters enclosed in either 'single' or "double" quotes*. You can find a list of named colors on wikipedia (https://en.wikipedia.org/wiki/Web_colors#Extended_colors), or use this tool (https://enes.in/sorted-colors/) to find the names of colors with a particular hue.

```
// fill the canvas with light blue
background('LightBlue');
```

* *Beware when pasting code from certain applications, some programs turn normal quote characters into “left and right” quote characters. Javascript won't like this.*


