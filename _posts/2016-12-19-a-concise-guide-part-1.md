---
layout: post
title:  A concise(ish) guide to Javascript, part 1
date:   2016-12-19
summary: A concise guide
categories: intro javascript ecosystem
---

*** WORK IN PROGRESS ***

Javascript (JS) is awesome. The community is awesome, the ecosystem is awesome, and how easily you can build cool stuff is awesome. However, Javascript fatigue is a real problem which stems from developers new and experienced alike having trouble keeping up with the changing ecosystem. Javascript the language itself is complex enough, but then stack on all the libraries, frameworks, bundlers, compilers, transpilers, linters, platforms and it's enough for anyone to get confused.

This article and the ones that proceed it are designed to sum up the different parts of the ecosystem to help new programmers get up to speed more quickly. Although each one of them requires a lot of time to become an expert, and very few people (actually, probably noone) understands them all a super high level, these articles can be kind of a "reference" to help you get the gist of each part. Let's dive in!


### ECMAScript and JavaScript

JavaScript, ECMA? ES6, ES2017? What?

Confusing, but easy to clear up!

ECMAScript is name of the official _specification_ for a scripting language. It basically says "if you make a language that follows all these rules, it counts as an ECMAScript _implementation_". Implementation just means the thing you created actually works. Specs are like building plans, implementations are like buildings.

JavaScript is the de-facto ECMAScript implementation, meaning it's the one that everyone uses. Long ago there used to be competing implementations, but now people us ECMAScript and JavaScript pretty interchangeably.

Before recently, the version of ECMAScript was defined with a single number. ES3 was version three, ES6 was version 6 etc. Since JavaScript is now super popular, the folks who maintain the spec decided to make a release every year. Hence, ES2016 is the release for 2016, ES2017 is for 2017, etc. We won't dive in now, but this release cycle has certain implications with other tools you might use, but don't worry for now!

### Browser, Node etc.

Node? Browsers? Modules? Bundlers? V8? Minifiers? What?


#### Browsers
Let's slow down and go back to the old school. Originally, JavaScript was designed and intended to run on websites. That's it. Furthermore, it wasn't really intended to create rich applications in the way we use it now...it was to write small scripts to add some cool features to a web page that was mostly text.

The original way to include JavaScript on a webpage was to put a 'script' tag in the HTML, like so:

```HTML
<html>
<head>
    <script>
      ...some JavaScript
    </script>
</head>
<body>
  My cool page!
</body>
</html>
```

This was great for the browser and simple sites, and will still work just fine today!

But how do browsers understand and run the Javascript? The answer: With a Javascript Engine! A Javascript engine just takes Javascript and turns it into different code that the browser can run. It's obviously a little more complicated, but a fine summation is a JS engine translates JS into machine-code.

Each browser uses their own Javascript Engine. Chrome uses V8, FireFox uses SpiderMonkey, IE uses Chakra, etc.
