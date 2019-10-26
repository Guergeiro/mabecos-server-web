# mabecos-server-web
This repository contains the website of [mabecos-server](https://github.com/Guergeiro/mabecos-server).
## Table of Contents
- [Current Layout](https://github.com/Guergeiro/mabecos-server#current-layout)
- [Contribute](#contribute)
- [Copyright and License](#copyright-and-license)

## Contribute
To contribute to this repository you need:
- [Fork this repository](#fork)
- [Have TypeScript](#typescript)
### TypeScript
Even though Node.js runs JavaScript and TypeScript is just syntax sugar, it will greatly improve development as we are able to find type errors before they fail testing.

Another reason why TypeScript is demanded is for better understanding of the code. Take the following code as an example:
``` JavaScript
const function = (variable) => {
    ...
}
```
What is `variable`? Is it an array? A string? Should we get the type and change the behaviour of the function based on this? (This is really bad programming aproach btw).

Now check the next code:
``` TypeScript
const function = (variable: Array<string>) => {
    ...
}
```
What is `variable`? It is an array of with elements of type `string`! Easy! That's why TypeScript is so cool.

Okay, you can understand better the code, but how will this help in development?

Well, you can spot errors earlier! Check the following code (using the functions above):
``` JavaScript
const variable = 1;
function(variable);
```
Here, in JavaScript, you would only spot this error while running it. Whereas in TypeScript you would get a type error. And to further improve this you can:
``` TypeScript
const variable: Array<string> = ["hello", "world"];
function(variable);
```
Perfect. Is it too much? Well, it kinda is. Does it help? Definitly!
## Copyright and License
Copyright and License under [AGPL-3.0](https://github.com/Guergeiro/mabecos-server-web/blob/master/LICENSE)
