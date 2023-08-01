# Http

## 引入Http模块

```js
const fs = require('fs');

const http = require('http');

const path = require('path');
```

## 请求头Map对象

```js
// 请求头集合
const contentTypes = {'ico': 'image/x-icon', 'html': 'text/html;charset=utf-8', 'css': 'text/css', 'js': 'application/x-javascript'};
```

## 创建一个Http服务

```js
const server = http.createServer( function ( req, res) {

    const url = req.url;
    console.log( `请求地址: ${ url }` );

    // 获取文件的扩展名
    const extname = path.extname( url ).slice( 1 );
    console.log( `地址后缀名: ${ extname }` );

    // 获取请求头
    const contentType = contentTypes[ extname ] ?? '';
    console.log( `返回的contentType: ${ contentType }` );

    // 设置请求头
    res.setHeader( 'content-type', contentType  );

    // 获取资源文件的地址
    const realPath = path.resolve( __dirname, 'html', url === '/' ? 'index.html' : url.slice(1) );
    console.log( `请求文件的绝对地址: ${ realPath }` );

    console.log( '----------------------------------------------------------------------------------------' );

    // 调用fs模块获取资源数据
    const chunk = fs.readFileSync( realPath );

    // 返回请求数据
    res.end( chunk );

} );
```

## 监听Http端口

```js
server.listen( 3000, () => {

    console.log( '服务启动成功, 地址: http://localhost:3000' );

} );
```

