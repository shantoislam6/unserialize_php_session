# unserialize_php_session

`unserialize_php_session` is a lightweight JavaScript library for decoding serialized PHP session data. It can be used in both browser and Node.js environments

## Installation

```sh
npm i unserialize_php_session
```
or
```sh
yarn add unserializer
```
or
```sh
pnpm i unserializer
```

Alternatively, you can include the unserializer.js file directly in your HTML:
```html
<script src="path/to/unserializer.js"></script>
```

## Test

```sh
npm install -force && npm test
```

## Usage

```js
const unserializePhpSession = require('unserialize_php_session')

const serializedData = '62kf0k2a4minrtcbr6h1l104r2|a:5:{s:3:"bar";c:4:"name":2:{s:3:"foo";i:9;}s:4:"user";s:4:"foo2";s:6:"result";b:1;s:5:"group";i:9;s:9:"is_banned";i:0;}'

const decodedData = unserializePhpSession(serializedData)

console.log(decodedData)

/* output:
{
   '62kf0k2a4minrtcbr6h1l104r2': [
      bar: {
        name: [Array]
      },
      user: 'foo2',
      result: true,
      group: 9,
      is_banned: 0
    ]
}
*/

```
##### ***More example can see output of testing. `test/index.js`***

#### API

>`unserializer(text: string): object`

Decodes serialized PHP data and returns a JavaScript object.

-----

## Contributing

####Pull requests and bug reports are welcome! If you'd like to contribute, please follow these guidelines:

 ##### 1. Fork the repository.
 ##### 2. Create a new branch for your changes.
 ##### 3. Make your changes and add tests if applicable.
 ##### 4. Run npm test to ensure that all tests pass.
 #####  5. Submit a pull request.

  ### By contributing to this project, you agree to license your work under the same terms as the project itself (MIT).