# Path

## 引入path模块

```js
const path = require('path');
```

## 获取文件的绝对地址

```js
console.log( __filename ); // /Users/summer/Documents/code/Studys/nodejs/path.js
```

## 获取当前文件所在目录的绝对地址

```js
console.log( __dirname ); // /Users/summer/Documents/code/Studys/nodejs
```

## 获取当前文件的后缀名

```js
const name = path.extname( __filename );
console.log( name, name.slice(1) ); // .js js
```

## 拼接文件完整地址

```js
const relPath = path.resolve( __dirname, 'path.js' );
console.log( relPath ); // /Users/summer/Documents/code/Studys/nodejs/path.js
```

## 获取当前文件名称或者文件夹名称(文件名带后缀)

```js
const filename = path.basename( __filename ); // __dirname
console.log( filename ); // __filename: path.js   __dirname: nodejs
```

## 获取文件的完整路径对象

```js
const fileInfo = path.parse( __filename );
console.log( fileInfo );
// {
//     root: '/',
//     dir: '/Users/summer/Documents/code/Studys/nodejs',
//     base: 'path.js',
//     ext: '.js',
//     name: 'path'
// }
```


