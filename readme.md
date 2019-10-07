## what is this

a class for creating "hotkey" or "cheat code" actions in the browser

## usage

instantiate the class and then pass in the keys you want to use as a cheat code in order as a comma-separated string or an array of strings. call `start` on the instance when you want the cheat code to become active.

default timeout is one second! meaning that if you don't press a key in one second, the cheat code resets.

syntax:

```javascript
new cheatcode(code: string|array, callback: function [, delay: number])
```

example:

```javascript
let cheatCode = new cheatcode(
  "up, up, down, down, left, right, left, right, b, a, enter",
  () => {
    console.log("konami code entered");
  }
).start();
```
