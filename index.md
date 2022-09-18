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

  copyToClipboard("This Sring is Copied To Clipboard.");
```

#### A useful one-line JavaScript function, which can be used to easily copy any text to the clipboard.

---
