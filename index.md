---
title: "One-Line JavaScript Functions"
permalink: /
layout: default
---

# JavaScript Functions

In this repository, I have compiled a list of one-line JavaScript Functions that are used daily and needed by every developer.

## Let’s Start

---

### 1. Get a random boolean

```bash
  const RandomBoolean = () => Math.random() >= 0.5;
```

#### This function will return a boolean (true or false) using Math.random() method. It’s a 50/50 chance to get either true or false.

---

### 2. Copy to Clipboard

```bash
  const copyToClipboard = (text) => navigator.clipboard.writeText(text);
```

#### A useful one-line JavaScript function, which can be used to easily copy any text to the clipboard.

---

### 3. Scroll to Page Top

```bash
  const goToTop = () => window.scrollTo(0, 0);
```

#### Another useful JavaScript function in this list, which is used to automatically scroll to the top of the web page.

---

### 4. Generate Random Hex

```bash
  const randomHex = () => `#${Math.floor(Math.random() * 0xffffff).toString(16).padEnd(6, "0")}`;
```

---

### 5. Check Not-Empty String Array

```js
  const isNotEmptyStringArray = (arr) => return arr.indexOf("") === -1
```

#### You can validate user base information without long conditions with this function

---

#### You can generate random hex colors using this function.

---
