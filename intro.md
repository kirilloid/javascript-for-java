## Intro

This book assumes experience in real-world programming.

### Java-Script

You mean "Java Script"?

While the common wisdom is that "[JavaScript to Java is as carpet to car](https://stackoverflow.com/a/245068/255363)", it's not that they are completely unrelated languages. Even though, JavaScript was initially supposed to be much more like Scheme (which is a kind of LISP (if you know what I mean)), rather than a C-like language, at the last moment there was a sudden change to Java side.

There are some similar features/peculiarities between two languages, like a distant cousin has the same strangely-shaped nose. Do not expect similarities to be deep, but do not be surprised by such minor details.

> Shouldn't I start from TypeScript first?

Whilst [TypeScript](https://www.typescriptlang.org/) is a more appealing alternative, it is still JavaScript under the hood and I think understanding run-time behavior is important. Also type system and the whole language was developed to retrofit behavior of existing libraries so types there are more complex and they are different from Java or other similar languages.
It's similar for Kotlin / Clojure or whatever languages with both JVM and JavaScript compilation targets. They cannot hide quirks of JavaScript completely. You need to understand how to integrate your code with 3rd-party JavaScript libraries.

> Where can I get JavaScript runtime to play with?

Just press `F12` to open DevTools of your browser (yes, all desktop browsers have them, even IE) and switch to the "Console" tab. `Ctrl` + `Shift` + `J`. Moreover, these things are called DevTools for purpose. They have integrated debugger environment, profilers, inspectors various resources.
In real world development you might want to debug from _normal_ IDE, but actually development tools built into browsers are pretty decent ones, they even allow editing code and saving it back with some configuration.

> Is JavaScript enough for development real-world apps?

It might be enough for development, but topics covered in this book corresponds roughly to J2SE. In Java world, if one wants to develop a web application, it's necessary to know HTTP basics, some framework like Spring, standard APIs and so on.

> Where's the *official* documentation?

JavaScript is an open standard developed by no single corporation. If you want decent documentation in once place for development HTML sites/applications, there's [Mozilla Development Network](https://developer.mozilla.org/en-US/docs/Web/JavaScript). They also describe most browser APIs.
If you're targeting node.js development and their API [there's a separate site](https://nodejs.org/en/)

There's also [language specification](https://www.ecma-international.org/ecma-262/), but the former links are much better from practical standpoint. Reading specification is like reading HTTP-related RFCs if you're just going to implement REST API endpoint.