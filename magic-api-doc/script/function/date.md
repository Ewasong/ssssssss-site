---
subSidebar: false
---
# 日期函数

## date_format
- 入参：`target`:`Date`    日期
- 入参：`pattern`:`String` 格式
- 返回值：`Number`
- 函数说明：日期格式化
```js
return date_format(new Date());  // 2020-01-01 20:30:30
// return date_format(new Date(),'yyyy-MM-dd');  // 2020-01-01
```

## now
- 返回值：`Date`
- 函数说明：返回当前日期
```js
return now(); // 等同于 new Date();
```

## current_timestamp_millis
- 返回值：`long`
- 函数说明： 取当前时间戳(毫秒)
```js
return current_timestamp_millis(); // 等同于 System.currentTimeMillis();
```

## current_timestamp
- 返回值：`long`
- 函数说明： 取当前时间戳(秒)
```js
return current_timestamp(); // 等同于 current_timestamp_millis() / 1000;
```

