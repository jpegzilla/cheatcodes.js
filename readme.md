## what is this

a class for creating "hotkey" or "cheat code" actions in the browser

## usage

instantiate the class and then pass in the keys you want to use as a cheat code in order as a comma-separated string or an array of strings. call `start` on the instance when you want the cheat code to become active.

default delay is one second! meaning that if you don't press a key in one second after pressing the first key in the combination, the cheat code resets. you can change the delay if you'd like.

syntax:

```javascript
new cheatcode(code: string|array, callback: function [, delay: number])
```

valid keys: `a-z`, `0-9`, `f1-f12`, `up`, `down`, `left` and `right` arrow keys, `shift`, `space`, `minus`, `enter`, `ctrl`, `caps lock`, `alt`

example:

```javascript
let cheatCode = new cheatcode(
  "up, up, down, down, left, right, left, right, b, a, enter",
  () => {
    console.log("konami code entered");
  }
).start();
```
