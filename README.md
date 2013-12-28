# random-strings 0.0.1 [![Build Status](https://travis-ci.org/AndreasPizsa/node-random-strings.png?branch=master)](https://travis-ci.org/AndreasPizsa/node-random-strings)
## Fast, beautiful, unique random Strings for node

- __Fast.__ Integers only, no floating point operations. <3 your CPU!
- __Beautiful.__ Use your own character set or go with one of the ready-made ones. 
- __Unique.__ Uses the pseudo random number generator from node's `crypt` package.

## Usage

Easy:

```
npm install random-strings
```

```js
var rs = require('random-strings');

rs.random(20,'ABCD0987');   // ABCD0987
```

Done!

```
// Or use one of these:
rs.human(20);         // ABCDEFGHJKLMNPQRSTUVWXYZ23456789
rs.numeric(20);       // 0123456789
rs.hex(20);           // 0123456789ABCDEF
rs.base64(20);        // ABCDEFGHIJKLMNOPQRSTUVWXYZabcdefghijklmnopqrstuvwxyz0123456789-_
rs.newBase64(20);     // 0123456789ABCDEFGHJKLMNPQRSTUVWXYZ_abcdefghijkmnopqrstuvwxyz-+*$
rs.alphaUpper(20);    // ABCDEFGHIJKLMNOPQRSTUVWXYZ
rs.alphaLower(20);    // abcdefghijklmnopqrstuvwxyz
rs.alphaNumUpper(20); // ABCDEFGHIJKLMNOPQRSTUVWXYZ0123456789
rs.alphaNumLower(20); // abcdefghijklmnopqrstuvwxyz0123456789
rs.alphaNumMixed(20); // abcdefghijklmnopqrstuvwxyzABCDEFGHIJKLMNOPQRSTUVWXYZ0123456789


```


## Functions
### random(length[, alphabet])

Generate a String of `length` random characters from `alphabet`.

#### Parameters
`length` - Integer. The number of characters you want your String to be.

`alphabet` _optional._ String. The alphabet to use. Your resulting string will contain only characters from this alphabet. _Default:_ newBase64 character set (see below)

#### Returns
A String of `length` random characters from `alphabet`.

## Tips
- __Humans & Manual Processing__. Uppercase and Numerics only. Leave out 1lO0. Use ``randomStrings.human(length)``
- __Old Skool-ish eCommerce__. Be conservative about the length and use an uppercase (alpha)numeric character set. Use ``randomStrings.alphaNumUpper(16)`` or even ``randomStrings.numeric(16)``
- __Modern eCommerce (Bitcoin)__. Have fun! 64 characters and a full base64 character set = 64^64 options. Use ``randomStrings.base64(64)``
- __IDs, Tokens__ Yeeeeh! 64+ characters and a full base64 character set. Perfect for ``randomString.base64(128)``

## License

The MIT License (MIT)

Copyright (c) 2013 Andreas Pizsa.

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in
all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN
THE SOFTWARE.

