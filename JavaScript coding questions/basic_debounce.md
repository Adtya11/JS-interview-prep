
###problem link - https://bigfrontend.dev/problem/implement-basic-debounce

### Solution

```js
/**
 * @param {(...args: any[]) => any} func
 * @param {number} wait
 * @returns {(...args: any[]) => any}
 */
function debounce(func, wait) {
  // suppose delay is 2 seconds, fun will be called if it had been previously called in less than 2 seconds then fun will not
  // be executed.

  let timerId = null;
  return function (...args) {
    clearTimeout(timerId);

    timerId = setTimeout(() => {
      func(args);
    }, wait);
  }
}
```
