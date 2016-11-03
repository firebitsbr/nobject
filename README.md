# nobject

> Nested javascript objects

## Install

Install with [npm](https://www.npmjs.com/)

```sh
$ npm i nobject --save
```

## Usage

```js
const Nobject = require('nobject');

const myNobject = new Nobject

// Set values either by array or just by argument
myNobject.set(['a', 'a', 'a'], 1)
myNobject.set('a', 'a', 'b', 2)

// Get values the same way
myNobject.get('a', 'a', 'a')
// >> 1
myNobject.get(['a', 'a', 'b'])
// >> 2
myNobject.get('x', 'y')
// >> undefined

// Crawl a nobject just like an array
myNobject.forEach((keys, value) => {
  console.log(keys, value)
  if (/* done iterating */)
    return false
  else
    return true //or anything other than false
})
// >> ['a', 'a', 'a'] 1
// >> ['a', 'a', 'b'] 2

// Output JSON
myNobject.toJSON()
// >> { "a" : { "a" : { "a" : 1, "b" : 2 } } }




```

## Running tests

Install dev dependencies:

```sh
$ npm i -d && npm test
```

## Contributing

Pull requests and stars are always welcome. For bugs and feature requests, [please create an issue](https://github.com/SafeMarket/nobject/issues)


## License

Copyright © 2016 []()
Licensed under the MIT license.

***

_This file was generated by [readme-generator](https://github.com/jonschlinkert/readme-generator) on November 03, 2016._