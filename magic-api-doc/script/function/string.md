---
subSidebar: false
---
# 字符串函数

## uuid
- 返回值: `String` `32`位无`-`的`UUID`
```js
return uuid(); // 等同于 UUID.randomUUID().toString().replace("-", "");
```
## is_blank
- 入参：`target`:`String`  判断的目标
- 返回值： `boolean`
- 函数说明：判断字符串是否为空
```js
return is_blank(''); // true 等同于 StringUtils.isBlank 一致
```

## not_blank
- 入参：`target`:`String`  判断的目标
- 返回值： `boolean`
- 函数说明：判断字符串是否不为空
```js
return not_blank(''); // false 等同于 !is_blank('')
```
