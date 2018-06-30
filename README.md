# Stemmer for Ukrainian language
Stemmer for Ukrainian language in Node.js. Adapted from algorithm implementation for Drupal by Algenon (4algenon@gmail.com): https://drupal.org/project/ukstemmer

You can also use strict mode to take into consideration alterations of consonants

## Usage

```bash
npm install Amice13/ukrstemmer-node --save
```

```js
var stemmer = require('ukrstemmer-node');

console.log(stemmer('випробування')); // 'випробуван'
console.log(stemmer('Чепинога')); // 'чепиног'

console.log(stemmer('Чепинога', strict = true)); // 'чепино'
console.log(stemmer('Чепинозі', strict = true)); // 'чепино'

// Caution!

console.log(stemmer('нога', strict = true)); // 'но'
console.log(stemmer('нозі', strict = true)); // 'но'
console.log(stemmer('ніжка', strict = true)); // 'ніжк'

```
