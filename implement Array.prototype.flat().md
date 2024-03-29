
###problem link - https://bigfrontend.dev/problem/implement-Array-prototype.flat

### Solution

```js
// This is a JavaScript coding problem from BFE.dev 


type Func = (arr: Array<any>, depth?:number) => Array<any>

const flat: Func = function (arr, depth = 1) {
  // your imeplementation here
  return arr.reduce((result, item) => {
    if(Array.isArray(item) && depth > 0) {
      result.push(...flat(item, depth - 1));
    }
    else {
      result.push(item);
    }
    return result;
  }, []);
}
```
