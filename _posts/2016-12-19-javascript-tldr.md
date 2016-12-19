---
layout: post
title:  "JS TL;DR"
date:   2016-12-19
tags: ['intro', 'javascript', 'ecosystem']
author: "Nick Kennedy"
---

This is everything I know about JavaScript in TL;DR form. JS is great, the ecosystem is huge and hard for beginners. Gain some sanity here. More in-depth writing can be down in the series of articles I'm writing called "A concise(ish) guide to JavaScript".


### Begin

JavaScript(JS) is a programming language originally designed for the web.

ECMAScript(ES) is the _specification_ for the language. JavaScript is the de-facto implementation. Specifications are like building plans, the implementation is like the building.

ES used to update infrequently, and used a number for its version. ES3 was version 3, ES5 version 5 etc. Now that JS is so crazy popular ES is updating every year, hence ES2016 and ES2017.

Broswers run JS by running them through a Javascript Engine, which turns JS into a different code the browser can execute on a computer. Every major browser uses a different JS Engine (Chrome - V8, Firefox - SpiderMonkey, IE - Chakra, etc).

JS used to be added to a webpage with a simple script tag. This still works and is all you need for super simple apps or prototyping. It looks like this in HTML:

```html
<html>
<head>
    <script type="text/javascript">
      ...some JS
    </script>
    <!-- or -->
    <script type="text/javascript" src="someJSfile.js">
    </script>

</head>
<body>
  My cool page!
</body>
</html>
```

Modules, frameworks, and libraries are all fundamentally the same thing but are used for different purposes.

Modules are a way of breaking your code into pieces to make it more re-usable and readable. If you have 3 functions, you can split them into 3 modules.

A module is generally your own code that you split up to make it more reusable and easy to think about instead of having one giant file with 1000s of lines of code.

A library is someone else's code you want to use that helps accomplish a specific set of tasks. It is like a swiss army knife. It doesn't tell you how to use the functions or how to build your app, it just makes common calculations/operations more straightforward. Think like a math library, a date library, etc.

A framework is also someone else's code but designed around guiding you towards a specific design pattern. Quite literally a framework for an application. It says "this is a good way to build apps, here are a bunch of helper functions to make that easy for you".

People often use library/framework interchangeably but the fundamental difference is above. Just someone else's code you're bringing into your own project because it's better/already done/tested by a bunch of people.

Node is a JS Runtime that uses Chrome's V8 Engine to let you run JS code on a computer or server directly rather than in a browser. It also lets you do cool things like read/write files or use sockets, something you can't really do as easily with code in a browser.

JS didn't have an official module specification until very recently (ES2016). What does this mean? Before the only way to get code was to add more script tags in the browser. They had to be in the right order if a library had a dependency on another library, and wouldn't always work properly. By dependency I mean the library or framework needs another framework/library to function properly, so it has to be loaded first.

When node started getting popular, people decided to maintain and release their own module specification called CommonJS. This was to let people import/export modules and libraries locally similar to the way they were used to doing it with other languages like C, Java, Etc. The syntax looked like this:

```javascript
var myLibrary = require('library');
```

This would pull in whatever was in `library.js` and exported on the module object. `library.js` needed to have this at the end:

```
module.exports = {
  stuff
}
```

Basically library would expose an object, and using 'require' would allow you use this object inside another JS file. This was a much better setup thank using many many link tags!

To help manage all these libraries and libraries that have dependencies, Node Package Manager(NPM) was created. NPM is basically a program that you can run and say "I am starting a JS project, let me download and use libraries/frameworks if I need them."

NPM uses a JSON configuration file called package.json to understand how libraries and frameworks work and resolve all the dependencies and flatten them. This means it looks at your package.json file, and looks at all the dependcies you've listed, then looks at the dependecies of all those packages, until it goes all the way down the chain and downloads all the right stuff. A big improvement over script tag!

The package.json file makes it really easy for someone else to download your project and use it, tweak it, or work on it.

Git is a system for doing _version control_. This means that multiple people can edit the set of files without screwing things up. All the changes you make are tracked, reversible, etc.
