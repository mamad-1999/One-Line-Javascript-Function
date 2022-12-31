---
title: "One-Line JavaScript Functions"
permalink: /
layout: default
---

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

### 15. Split a string by 3 characters

```js
const splitedBy3CharString = (str) => str.match(/.{1,3}/g);
console.log(splitedBy3CharString("123456789"));
// Result => ['123', '456', '789']
```

#### You can mask an input with this function.

- Tip: You can enter one number you want instead of `3` on the regex above.

---

### 16. Add space between characters of a string

```js
const spaceBetweenChars = (str) => str.split("").join(" ");
console.log(spaceBetweenChars("javascript"));
// Result => j a v a s c r i p t
```

---

### 17. Paste from clipboard to inner tag

```js
const GetCopiedClipboardValue = (element) =>
  navigator.clipboard.readText().then((txt) => (element.innerHTML = txt));
console.log(GetCopiedClipboardValue(document.querySelector("p")));
```

#### You can paste current clipboard value with this function

---

### 18. Check if the user is on an Apple device

```js
const isAppleDevice = /Mac|iPod|iPhone|iPad/.test(navigator.platform);

console.log(isAppleDevice);
```

#### As in a lot of projects, we need to implement device-based features. You can use this function to make sure that the user is using an Apple device or not.

---

### 19. Strip HTML From Text

```js
const stripHtml = (html) =>
  new DOMParser().parseFromString(html, "text/html").body.textContent || "";

console.log(stripHtml("<h1>Hello <strong>World</strong>!!!</h1>"));
// Result: Hello World!!!
```

---

### 20. Remove Duplicates in an Array

```js
const removeDuplicates = (arr) => [...new Set(arr)];

removeDuplicates([11, 56, 22, 11, 45, 22, 11]);
//[ 11, 56, 22, 45 ]
```

---

### 21. Get the Average of an Array of Number

```js
const average = (arr) => arr.reduce((a, b) => a + b) / arr.length;

average([11, 36, 63, 167, 32]);
//61.8
```

---

### 22. Get Query Params from URL

```js
const getParameters = (URL) =>
  JSON.parse(
    '{"' +
      decodeURI(URL.split("?")[1])
        .replace(/"/g, '\\"')
        .replace(/&/g, '","')
        .replace(/=/g, '":"') +
      '"}'
  );

getParameters("https://www.google.de/search?q=animals&start=30");
// Result: { q: 'animals', start: '30' }
```

#### Very useful function when you are dealing with url, query parameters. You can easily retrieve query parameters from a url by passing, url as the argument of the function.

---

### 23. Detect Dark Mode

```js
const isDarkMode =
  window.matchMedia &&
  window.matchMedia("(prefers-color-scheme: dark)").matches;

console.log(isDarkMode); // Result: True or False
```

#### Find out if a user’s device is in dark mode, using the following code.

---

### 24. Get a random number in a specific range

```js
const randomNumberInRange = (min = 0, max = 1000) =>
  Math.floor(Math.random() * (max - min + 1)) + min;

randomNumberInRange();
// Result: Default random number range is 0 - 1000, so you get a number between 0 and 1000.
randomNumberInRange(100, 2000);
// Result: You will get a random number between 100 and 2000, where 100 is min range and 2000 is max range.
```

#### An essential JavaScript function to generate a random number between a specific range of numbers. You provide a minimum and a maximum value as arguments and the one-line function returns a random number from the given range.

---

### 25. Check if a variable is an array

```js
const isArray = (arr) => Array.isArray(arr);

isArray([1, 2, 3]);
```

---

### 26. Generate a random string

```js
const randomString = () => Math.random().toString(36).slice(2);
```

---

### 27. Convert Fahrenheit / Celsius

```js
const celsiusToFahrenheit = (celsius) => (celsius * 9) / 5 + 32;
const fahrenheitToCelsius = (fahrenheit) => ((fahrenheit - 32) * 5) / 9;

// Examples
celsiusToFahrenheit(15); // 59
celsiusToFahrenheit(0); // 32
celsiusToFahrenheit(-20); // -4

fahrenheitToCelsius(59); // 15
fahrenheitToCelsius(32); // 0
```

#### Dealing with temperatures can be confusing at times. These 2 functions will help you convert Fahrenheit to Celsius and the other way around.

---

### 28. Remove falsy values from array

```js
const removeFalsyValue = (arr) => arr.filter(Boolean);
```

---

### 29. Convert radians to degrees && degrees to radians

```js
const radsTodegs = (rad) => (rad * 180) / Math.PI;
const degsTorads = (deg) => (deg * Math.PI) / 180.0;
```

---

### 30. Deep Copy an Object with ease

```js
const deepCopy = (obj) => JSON.parse(JSON.stringify(obj));
```

#### You can deep copy any object by converting it to a string and back to an object. This will work, not only with objects but other composite data types as well like Arrays.

---

### 31. wait function

```js
const wait = (ms) => new Promise((resolve) => setTimeout(resolve, ms));
const asyncFunc = async () => {
  await wait(1000);
  console.log("async");
};
asyncFunc();
```

---

### 32. Go Back to the Previous Page

```js
const navigateBack = () => history.back();
// Or
const navigateBack = () => history.go(-1);
```

#### Need to send the user back to the page they came from? history object to the rescue!

---

### 33. Check if an Element is Focused

```js
const hasFocus = (element) => element === document.activeElement;
```

#### You can effortlessly check if an element is currently focused without setting up the focus & blur listener.

---

### 34. Text to speech

```js
const sound = (text) => {
  var msg = new SpeechSynthesisUtterance();
  msg.text = text;
  window.speechSynthesis.speak(msg);
};
```

---

### 35. Create UUID without any libraries

```js
const createUUIDv4 = () => crypto.randomUUID();
```

---
