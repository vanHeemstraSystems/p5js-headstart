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

Multi-line comments start with a forward slash followed immediately by an asterisk (a.k.a. star character). As it's name implies a multi-line comment can by spread out over multiple lines, and it doesn't end until there is another asterisk followed by a forward slash. (Note: multi line comments can also be used on a single line, with the advantage that more code can come after the end of the comment.

Comments don't do anything when a sketch runs, but they are useful for explaining what the code around them is doing, and you'll see a lot of them in this tutorial.


