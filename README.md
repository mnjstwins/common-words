# common-words [![NPM version](https://badge.fury.io/js/common-words.png)](http://badge.fury.io/js/common-words)

> Updated list (JSON) of the 100 most common words in the english language. Useful for excluding these words from arrays.

From <https://en.wikipedia.org/wiki/Most_common_words_in_English>

Example:

```js
[
  {
    "rank": "1",
    "word": "the"
  },
  {
    "rank": "2",
    "word": "be"
  },
  {
    "rank": "3",
    "word": "to"
  },
  ...
]
```

## Install
Install with [npm](npmjs.org):

```bash
npm i common-words --save-dev
```

## Usage

```js
var common = require('common-words');

function removeCommonWords(words, common) {
  common.forEach(function(obj) {
    var word = obj.word;
    while (words.indexOf(word) !== -1) {
      words.splice(words.indexOf(word), 1);
    }
  });
  return words;
};
removeCommonWords(yourWords, common);
```

## Author

**Jon Schlinkert**

* [github/jonschlinkert](https://github.com/jonschlinkert)
* [twitter/jonschlinkert](https://twitter.com/jonschlinkert)


## License
Copyright (c) 2014 Jon Schlinkert, contributors.
Released under the MIT license

***

_This file was generated by [verb-cli](https://github.com/assemble/verb-cli) on April 13, 2014._