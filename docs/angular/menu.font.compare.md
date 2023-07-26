# 业务中心菜单和Iconfont图标库图标对比

> Iconfont图标库有大约1000个图标, 然后业务中心的菜单大约有500多个菜单, 现在要找出菜单里面的图标没有在Iconfont图标库中的

1. 下载iconfont.json到本地

2. 拿到业务中心的所有菜单的JSON数据, 保存在menu.json文件中

3. 用nodeJs中的fs模块读取文件, 进行数据对比

> 以下为代码示例: 

## 导入nodeJs中的fs模块

```js
const fs = require('fs');
```

## 读取iconfont.json里面的数据

```js

const iconfontBuffer = fs.readFileSync( './iconfont.json' );

const iconfontBufferString = iconfontBuffer.toString();

const iconfontObject = JSON.parse( iconfontBufferString );

const { glyphs } = iconfontObject;

const iconfontClasses = glyphs.map( item => item['font_class'] );

console.log( iconfontClasses );

```

!> 注意这里传入的iconfont.json为相对路径

## 读取menu.json里面的数据

```js
const menuBuffer = fs.readFileSync( './menu.json' );

const menuBufferString = menuBuffer.toString();

const menuList = JSON.parse( menuBufferString );

console.log( iconfontClasses );
```

!> 注意这里传入的menu.json为相对路径

## 进行数据对比

```js

const needMenuIconList = [];

for ( let i = 0; i < menuList.length; i++ ) {
    
    const menuListItem = menuList[ i ];
    
    const { appMenuPhoto, appMenuName } = menuListItem;
    
    if ( iconfontClasses.includes( appMenuPhoto ) ) continue;
    
    needMenuIconList.push( { 'icon': appMenuPhoto, 'name': appMenuName } );
    
}
console.table( needMenuIconList );

```

## 执行命令

```shell
node compare.js
```

