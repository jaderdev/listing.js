# listing.js

A JavaScript library for working with comma separated lists

[![NPM](https://nodei.co/npm/listing.js.png)](https://nodei.co/npm/listing.js/)

## Introduction:

listing.js is a library that simplifies the work with comma separated lists in JavaScript. Most of the features are similar to those of array methods. Besides commas, other delimiters are supported as well.

## Installation:

Install via npm

```
npm i --save listing.js
```

## Usage:

```javascript
const Listing = require('listing.js');
// ES6: import Listing from 'listing.js';

const myList = new Listing('1,2,3,4');
myList.append(5);

// 1 2 3 4 5
for (const val of myList) console.log(val);
```

## Valid delimiters and lists:

listing.js currently supports six different delimiters. In this case, each number is a single list item.

```javascript
const Listing = require('listing.js');

const myList1 = new Listing('1,2,3,4'); // ,
const myList2 = new Listing('1;2;3;4'); // ;
const myList3 = new Listing('1:2:3:4'); // :
const myList4 = new Listing('1-2-3-4'); // -
const myList5 = new Listing('1_2_3_4'); // _
const myList6 = new Listing('1.2.3.4'); // .
```

You can also use strings instead of numbers as items:

```javascript
const Listing = require('listing.js');

const myList = new Listing('hello,I,am,John');
```

The list items are accessible via the `.list` property.
Example:

```javascript
const Listing = require('listing.js');

const myList = new Listing('1,2,3');
console.log(myList.list); // Expected output: 1,2,3
```

## Documentation

You can find the complete documentation [here](https://larswaechter.github.io/listing.js/).

## Contributing

See [CONTRIBUTING.md](https://github.com/larswaechter/listing.js/blob/master/CONTRIBUTING.md)

## License

[MIT](https://github.com/larswaechter/listing.js/blob/master/LICENSE)
