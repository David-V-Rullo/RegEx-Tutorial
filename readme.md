# RegEx Tutorial

## What is RegEx

RegEx, or REGular EXpression is a method to search through strings of text in order to detect patters of characters. Using RegEx you can do all sorts of fun things with your code, such as search and replace, pattern matching, and validation. RegEx can be used for the simplest searching, for example just searching for a word, all the way up to finding complex patterns of characters in a document.

## How do you use RegEx?

RegEx uses a simple syntax which can achieve some really impressive results in the hands of a capable programmer. 

The simplest RegEx syntax would be this: 

`/a/`

This would simply search a document for any occurances of the letter 'a'. The forward slashes denote the beginning and the end of the RegEx statement. You could place any word in between the slashes to find that word in a document. But that would require the word to be spelled correctly or else the RegEx will not work. 

An example would be: 

`/sign/`

This would be great if you were looking for the word sign in a proofread document, but what if you had an author that frequently makes the mistake of writing sing instead of sign. Then you would be out of luck. 

But with some forward thinking RegEx, you could solve your little problem by writing the following: 

`/si(ng|gn)/`

While this is a simple example, it shows just how RegEx can be employed by using simple operators such as the parenthese '()' and the vertical bar '|'. 

## RegEx Components

There is a suite of tools to be used in crafting an elegant RegEx statement. Below are some of the most basic and easily accessible. 

### Anchors

Anchors are used for exactly the purpose you would think. They anchor the search to the position within the string you want to search. 

The `^` will match any leading characters in a string. It will grab whatever characters you put after it, then search for any word or term that contains those characters with any number of characters after it, but not before it. For example: 

`/^boot/` 
Would give you a result that inluded 'boot', 'bootcamp', 'bootstrap', 'booth' or 'bootffffffffffffffffffffff' if that is your kind of thing. 

The `$` works much the same way as the `^` however this anchor will return all the preceeding characters to your search. For example:

`/$camp/`
Would give you 'bootcamp' but not 'campground'. Again this is basic stuff but its usefulness is invaluable. 

### Quantifiers

Using `*` will return a matching string that ends with zero or more of the character preceeding the `*`. So `/abc*/` will return any string that contains 'ab' and ends with any number of 'c' or no 'c' at all. 


Using the above example you can see how the other quantifiers work. 

`/abc+/` gives you 'ab' followed by one or more 'c'.

`/abc?/` gives you 'ab' followed by either no 'c' or one 'c'.

`/abc{2}/` gives you 'ab' followed by two 'c' characters.

`/abc{2,}/` gives you 'ab' followed by two or more 'c' characters.

`/abc{2,4}/` gives you 'ab' followed by at least two 'c' characters and no more that four 'c' characters. 

These quantifiers can be combined in a variety of ways and along with grouping are the basis of RegEx. 

### Grouping

As with anything related to coding or math, grouping plays an important role. The most common form of grouping in RegEx is the bracket '[]'. Allowing you to capture any character in the bracket. 

For example: 

`/a[bc]/` will give you a result where a is followed by either a 'b' or a 'c'. Which doesn't seem useful, but if you wrote it like this: 

`/a[a-zA-Z]/` you could capture the entire alphabet, upper and lowercase, after the 'a'. This grouping would help you capture email adresses and other validation methods. 

### Classes

By using a backslash '\' you can use search specific character classes. The backslash serves as an escape character, allowing you to use the search character without searching for that actual character, for example: 

`/d/` would search for the letter 'd', which `/\d/` would search for any single digit. 

Fundamental classes, including the above 'digit' search are: 

`/\w/` searches for an entire word character. Be careful though, this will also return gibberish since it is only looking for "words" as it understands them not "words" in how we understand them e.g. "asdfasd" is not differentiatied from "cat". 

`/\s/` searches for spaces. Its a whitespace finder if that is your kind of thing. 


## Conclusion 

RegEx is an invaluable tool for developers and with some practice you can wield it like a pro. Look below to test your new skills. 

`/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/` is the expression for capturing most email addresses. Using the above lessons, see if you can pick it apart. 

## Author

David Rullo is a soon to be junior full-stack web developer.

For more check out:

[Regex Playground](https://regexr.com/)

[Regex MDN Page](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Regular_Expressions/Cheatsheet)