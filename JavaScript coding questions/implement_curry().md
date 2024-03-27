
###problem link - https://bigfrontend.dev/problem/implement-curry

### Solution

```js
// This is a JavaScript coding problem from BFE.dev 

/**
 * @param { (...args: any[]) => any } fn
 * @returns { (...args: any[]) => any }
 */
function curry(func) {
  return function CurriedFunction(...args) {
    if(args.length >= func.length) {
      return func.call(this, ...args);
    }
    else {
      return CurriedFunction.bind(this, args);
    }
  }
}
```
