---
subSidebar: false
---
# magic

## 引用模块
```javascript
import magic;
```
## call
- 入参：`method`:`String`  定义的请求方法
- 入参：`path`:`String`  定义的路径
- 入参：`parameters`:`Map` 变量信息
- 返回值：`Object`
- 函数说明：执行MagicAPI中的接口,返回值带code和message信息
```js
return magic.call('get','execute/sql',{
    message : 'Hello,Magic API!' //传入参数 
})
```
## execute
- 入参：`method`:`String`  定义的请求方法
- 入参：`path`:`String`  定义的请求路径
- 入参：`parameters`:`Map` 变量信息
- 返回值：`Object`
- 函数说明：执行MagicAPI中的接口,返回原始内容，不包含code以及message信息
```js
return magic.execute('get','execute/sql',{
    message : 'Hello,Magic API!' //传入参数 
})
```

## invoke
- 入参：`path`:`String`  函数路径
- 入参：`parameters`:`Map` 变量信息
- 返回值：`Object`
- 函数说明：执行MagicAPI中的函数
```js
return magic.invoke('get','/test/add',{
    a: 1,
    b: 2
})
