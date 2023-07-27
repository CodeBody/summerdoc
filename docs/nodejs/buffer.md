# Buffer

## 创建一个长度为10的Buffer

```js
const buf1 = Buffer.alloc( 10 );
console.log( buf1 ); // <Buffer 00 00 00 00 00 00 00 00 00 00>
```

## 创建一个长度为10的Buffer并且填充数据

```js
const buf2 = Buffer.alloc( 10, 1 );
console.log( buf2 ); // <Buffer 01 01 01 01 01 01 01 01 01 01>
```

## 创建一个长度为10的Buffer 默认不初始化 通过fill方法填充值

```js
const buf3 = Buffer.allocUnsafe( 10 );
buf3.fill( 1 );
console.log( buf3 ); // <Buffer 01 01 01 01 01 01 01 01 01 01>
```

## 英文转Buffer

```js
const buf4 = Buffer.from( 'hello' );
console.log( buf4 ); // <Buffer 68 65 6c 6c 6f>
```

## Buffer转英文

```js
const buf5 = Buffer.from( [ 0x68, 0x65, 0x6c, 0x6c, 0x6f ] )
console.log( buf5.toString() ); // hello
```

## 汉字转Buffer

```js
const buf6 = Buffer.from( '张三' );
console.log( buf6 ); // <Buffer e5 bc a0 e4 b8 89>
```

## Buffer转汉字

```js
const buf7 = Buffer.from( [ 0xe5, 0xbc, 0xa0, 0xe4, 0xb8, 0x89 ] );
console.log( buf7.toString() ); // 张三
```

