# Fs

## 引入fs模块

```js
const fs = require('fs');
```

## 引入path模块

```js
const path = require('path');
```

## 声明需要读写的文件地址

```js
const filename = path.resolve( __dirname, 'fs', 'fs.md' ); // /Users/summer/Documents/code/Studys/nodejs/fs/fs.md
```

## 写入文件 - writeFile

```js
fs.writeFile( filename, 'writeFile', err => {
    if ( err == null ) return console.log( '写入成功' );
    console.log( err );
} )
```

## 写入文件 - writeFileSync

```js
fs.writeFileSync( filename, 'writeFileSync' );
```

## 写入文件 - createWriteStream

```js
const stream = fs.createWriteStream( filename );
stream.write( 'createWriteStream1' );
stream.write( 'createWriteStream2' );
stream.close();
```

## 追加文件 - appendFile

```js
fs.appendFile( filename , 'appendFile', err => {
    if ( err == null ) return console.log( '追加成功' );
    console.log( err );
} );
```

## 追加文件 - appendFileSync

```js
fs.appendFileSync( filename, 'appendFileSync' );
```

## 读取文件 - readFile

```js
fs.readFile( filename, function ( err, chunk ) {
    if ( err != null ) return console.log( '读取失败...', err );
    console.log( chunk.toString() );
} )
```

## 读取文件 - readFileSync

```js
const  chunk = fs.readFileSync( filename );
console.log( chunk.toString() );
```

## 读取文件 - createReadStream

```js
const readStream = fs.createReadStream( filename );
let data = '';
readStream.on( 'data', function ( chunk ) {
    data += chunk;
} )
readStream.on( 'end', function () {
    console.log( data.toString() );
    readStream.close();
} )
```

## 删除文件 -- unlink

```js
fs.unlink( filename, err => {
    if ( err != null ) return console.log( '删除失败...', err );
    console.log( '删除成功' );
} );
```

## 删除文件 -- unlinkSync

```js
fs.unlink( filename );
```

