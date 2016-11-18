#Template Strings / Template Literials

>Synstax Sugar or a New Construct to the language?
>Know the difference? 

```function doubleMessage(number) {
  return `Your number doubled is ${(2 * number)}`;
}```
###Looks super sexy huh? 'Cause it is!

Old way plus the flaws. Need to concatenate and escape characters. 

```
console.log("string text line 1\n"+
"string text line 2");
// "string text line 1
// string text line 2"
```

Lets take a long at some code we might actually write today with ES5. 
```
function getYear(){
	const year = new Date().getFullYear();
	return "The year is " + year;
}
getYear(); // The year is 2016 
```

Now lets rewrite this code with template strings. The syntax will look a lot nicer than before. Nothing is going to change other than instead of double or single quotes, we are going to use the ` (backtick/backquote) Inside there backtiacks we will use ${} to inject our JavaScript expressions. 

```
function getYear(){
	const year = new Date().getFullYear();
	return `The year is ${year}`;
}
getYear(); // The year is 2016 SO USE 
```

If we have variable and want to do math to them, it's currently reather confusing and ugly.
We'd have to escape string and concatenate them with our variables.

```
var a = 5;
var b = 10;
console.log("The total is " + (a + b) + " and\nnot " + (2 * a + b) + ".");
// "Fifteen is 15 and
// not 20."
```

```
var a = 5;
var b = 10;
console.log(`The Total is ${a + b} and/nnot ${2 * a + b}.`);
```

```
var a = 26; // Total Questions in Quiz
var b = 18; // Total Answers marked right
console.log("The quiz is " + a + " questions and the student got " + b + " correct\n" +
 "Their score is " + (b / a).toFixed(2) + ".");
```


- ES2015
http://www.ecma-international.org/ecma-262/6.0/#sec-template-literals
- MDN
https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Template_literals