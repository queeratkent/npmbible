# NPMBible 


  Easy-to-use JS library for retrieving bible scripture. Cloned from [[@bricejlin\holy-bible](https://github.com/bricejlin/holy-bible)] but I forgot to fork it and instead just pushed it as a new repo. My bad !!


## Installation

  ```bash
  $ npm install npmbible --save
  ```

## Usage

  ```js
  var bible = require('npmbible');

  bible.get('John 15:13', 'ASV') // also supports 2-letter abbrev (ie: Jn 15:13)
    .then(function (res) {
      console.log(res.text);
    });

  // Greater love hath no man than this, that a man lay down his life for his friends.
  ```

## Documentation

###.get(verse [, version]) => Promise

######verse - A bible passage
  Type: `String`

######version - Bible version
  Type: `String`
  Default: `'ASV'`


######Resolves into an object
```js
{
  version: 'ASV',
  passage: 'John.15.13',
  text: 'Greater love...'
}
```
  
## Currently Supported Versions

  - ASV
  - KJV
  - NRSV

## Tests

  ```bash
  $ npm install
  $ npm test
  ```

## License

  [MIT](https://github.com/MadisonRWozniak/npmbible/blob/master/LICENSE)
