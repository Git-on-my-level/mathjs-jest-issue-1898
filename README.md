# mathjs-jest-issue-1898
Reproduce an issue involving mathjs and jest

Originally reported in:
https://github.com/josdejong/mathjs/issues/1898

Environment:
```
> node -v
v12.16.1
```

Steps to reproduce:
```
yarn install
yarn jest
```

Resulting error:
```
$ /Users/dazheng/temp/mathjs-jest-issue-1898/node_modules/.bin/jest
 FAIL  ./example.test.js
  ● Test suite failed to run

    TypeError: Cannot read property 'prototype' of undefined

    > 1 | import { std } from "mathjs";
        | ^
      2 | 
      3 | test("mathjs error", () => {
      4 |   console.log(std([10, 9, 11]));

      at createComplexClass.isClass (node_modules/mathjs/lib/type/complex/Complex.js:26:23)
      at Object.<anonymous> (example.test.js:1:1)
```
