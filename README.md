fonts.js
=========
fonts.js is an ascii art font framework written in coffeescript.

[![npm version][npm version]][npm link]
[![npm downloads][npm image]][npm link]
[![travis build status][travis image]][travis link]

How to use
----------
Install with `npm i fonts.js`

You can use this library in both coffeescript, and javascript:
```coffeescript
convert = require 'fonts.js'

str = 'HELLO\nWORLD'
console.log convert str, {font: 'lines'} # Lines is the default font.
```
```javascript
var convert = require('fonts.js');

var str = 'HELLO\nWORLD'
console.log(convert(str, {font: 'lines'})) // Lines is the default font.
```
```javascript
/*
Output (It looks better in a web page.):
_    _  ______  _      _      _______
| |  | ||  ____|| |    | |    |  ___  |
| |__| || |__   | |    | |    | |   | |
|  __  ||  __|  | |    | |    | |   | |
| |  | || |____ | |___ | |___ | |___| |
|_|  |_||______||_____||_____||_______|
_   _   _  _______  _____  _      _____
| | | | | ||  ___  ||  _  || |    |  __ \
| | | | | || |   | || |_| || |    | |  \ \
| | | | | || |   | ||    _|| |    | |   | |
| |_| |_| || |___| || |\ \ | |___ | |__/ /
|_________||_______||_| \_\|_____||_____/
*/
```

Making your own font
--------------------
Requirements:
* [Coffeescript](http://coffeescript.org/)

To make your own font:
* Step 1: Clone the [github repository](https://github.com/1p6/fonts.js/) into you own folder.
* Step 2: Create a coffeescript file under `src/fonts` with the name of your font as it's name.
* Step 3: Structure the file like the [default font](https://github.com/1p6/fonts.js/blob/master/src/fonts/lines.coffee). (Read the comments.)
* Step 4: Use the [fontCreater html page](https://github.com/1p6/fonts.js/blob/master/fontCreater.html) to help create each character.(Read bellow).
* Step 5: Add the name of your font to the font list in index.coffee
* Step 6: (Optionaly) Make a pull request so I can add the font.(Please test your font before you make a pull request though!(See bellow))

Making a character
------------------
* Step 1: Design your character in the textbox. IMPORTANT: Make sure each line is the same width!
  Otherwise the characters following it in a string will look weird.
* Step 2: Click the button.
* Step 3: Put it in your font file.

Testing your font (or anything else)
-----------------
Go to the root directory of the project and run `npm test`

[travis image]: https://img.shields.io/travis/1p6/fonts.js.svg
[travis link]: https://travis-ci.org/1p6/fonts.js
[npm image]: https://img.shields.io/npm/dm/fonts.js.svg
[npm link]: https://www.npmjs.com/package/fonts.js
[npm version]: https://img.shields.io/npm/v/fonts.js.svg
