# 配置多数据源


## 在线配置多数据源

![创建数据源](../.vuepress/public/images/create_datasource.png "创建数据源")

## 后台配置多数据源
```java
@Bean
public MagicDynamicDataSource magicDynamicDataSource(){
    MagicDynamicDataSource dynamicDataSource = new MagicDynamicDataSource();
    dynamicDataSource.setDefault(ds1); // 设置默认数据源
    dynamicDataSource.add("slave",ds2);
    return dynamicDataSource;
}
```

## 运行时动态配置数据源

在运行时只可以通过注入`MagicDynamicDataSource`对象来修改数据源信息
```java
@Autowired
private MagicDynamicDataSource magicDynamicDataSource;
// 此时可以通过调用magicDynamicDataSource的相关方法实现数据源的动态修改。
```
