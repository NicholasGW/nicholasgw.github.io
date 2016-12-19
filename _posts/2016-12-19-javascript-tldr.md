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

Node is a JS Runtime that uses Chrome's V8 Engine to let you run JS code on a computer or server directly rather than in a browser. It also lets you do cool things like read/write files or use sockets, something you can't really do as easily with code in a browser.
