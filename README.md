![js](https://user-images.githubusercontent.com/91375726/190903509-eedc8784-0e71-492e-8de6-dd667e044a27.png)

# 🚀 One-Line-Javascript-Function

In this repository, I have compiled a list of one-line JavaScript Functions that are used daily and needed by every developer.

## Let’s Start

---

### 1. Get a random boolean

```js
const RandomBoolean = () => Math.random() >= 0.5;
```

#### This function will return a boolean (true or false) using Math.random() method. It’s a 50/50 chance to get either true or false.

---

### 2. Copy to Clipboard

```js
const copyToClipboard = (text) => navigator.clipboard.writeText(text);
```

#### A useful one-line JavaScript function, which can be used to easily copy any text to the clipboard.

---

### 3. Scroll to Page Top

```js
const goToTop = () => window.scrollTo(0, 0);
```

#### Another useful JavaScript function in this list, which is used to automatically scroll to the top of the web page.

---

### 4. Generate Random Hex

```js
const randomHex = () =>
  `#${Math.floor(Math.random() * 0xffffff)
    .toString(16)
    .padEnd(6, "0")}`;
```

#### You can generate random hex colors using this function.

---

### 5. Check Not-Empty String Array

```js
const isNotEmptyStringArray = (arr) => arr.indexOf("") === -1;
```

#### You can validate user base information without long conditions with this function

---

### 6. Reverse a String

```js
const stringReverse = (str) => str.split("").reverse().join("");
```

#### You can reverse a string in one line using split, join, and reverse methods.

---

### 7. Capitalize a String

```js
const capitalize = (str) => str.charAt(0).toUpperCase() + str.slice(1);

capitalize("i love javascript.");
// I love javascript.
```

#### As JavaScript doesn’t provide a built-in capitalize method, using this one-line function you can capitalize a string.

---

### 8. Convert RGB to Hex

```js
const rgbToHex = (r, g, b) =>
  "#" + ((1 << 24) + (r << 16) + (g << 8) + b).toString(16).slice(1);

rgbToHex(255, 255, 255);
// "#ffffff"
```

#### A useful function on this list, which is used to convert the RGB to hex code.

---

### 9. Shuffle an Array

```js
const shuffleArray = (arr) => arr.sort(() => 0.5 - Math.random());

console.log(shuffleArray([1, 2, 3, 4, 5, 6, 7]));
// Result: [ 1, 4, 3, 2, 6, 5, 7 ]
```

#### You can use the following code to shuffle an array. It uses sort and random methods.

---

### 10. Find the day of the year

```js
const dayOfYear = (date) =>
  Math.floor((date - new Date(date.getFullYear(), 0, 0)) / 1000 / 60 / 60 / 24);

dayOfYear(new Date());
// Result: 262
```

---

### 11. Delete selected Item from the array

```js
const DeletedArray = (arr, sltItem) => arr.filter((item) => item !== sltItem);

console.log(DeleteArray(["google", "microsoft", "apple"], "apple"));
// Result => ['google', 'microsoft']
```

---

### 12. Get a random item from an array

```js
const randomArrayItem = (arr) => arr[Math.floor(Math.random() * arr.length)];
```

#### This one-liner returns you a random item from your input array, that you pass as an argument to the function.

---

### 13. Check if Date is Valid

```js
const isDateValid = (...val) => !Number.isNaN(new Date(...val).valueOf());

isDateValid("December 23, 2012 16:24:50");
// Result: true
```

#### Check the user date input validity, using this Js function.

---

### 14. Clear All browser Cookies

```js
const clearCookies = document.cookie
  .split(";")
  .forEach(
    (cookie) =>
      (document.cookie = cookie
        .replace(/^ +/, "")
        .replace(/=.*/, `=;expires=${new Date(0).toUTCString()};path=/`))
  );
```

---

### 15. Split a string by n characters

```js
const splitedBy3CharString = (str) => str.match(/.{1,3}/g);
console.log(splitedBy3CharString('123456789'));
// Result => ['123', '456', '789']
```

#### You can mask an input with this function.
- Tip: You can enter one number you want instead of `3` on the regex above.

---

### 16. Add space between characters of a string

```js
const splitedBy3CharString = (str) => str.split('').join(' ');
console.log(splitedBy3CharString('javascript'));
// Result => j a v a s c r i p t
```

---

### 17. Paste from clipboard to inner tag

```js
const GetCopiedClipboardValue = (element) => navigator.clipboard.readText()
.then(txt => element.innerHTML = txt);
console.log(GetCopiedClipboardValue(document.querySelector('p')));
```

#### You can paste current clipboard value with this function

---

## Contribution Guide

1. fork the repo
2. Edit index.md or Readme.md file (add new function)
3. submit PR
