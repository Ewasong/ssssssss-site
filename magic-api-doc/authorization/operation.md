# UI操作鉴权

```java
/**
 * 自定义操作鉴权
 */
@Component  //注入到Spring容器中
public class CustomAuthorizationInterceptor implements AuthorizationInterceptor {

	// 自定义登录的逻辑请参考上一篇文章
    
    // 对于登录走自身应用的，MagicUser 对象会为空，此时需要自己获取当前登录的用户信息。

	/**
	 * 配置是否需要登录
	 */
	@Override
	public boolean requireLogin() {
		return false; // 配置为不需要登录（走应用自身的登录）
	}

	/**
	 * 是否拥有页面按钮的权限
	 */
	@Override
	public boolean allowVisit(MagicUser magicUser, HttpServletRequest request, Authorization authorization) {
		// Authorization.SAVE 保存
		// Authorization.DELETE 删除
		// Authorization.VIEW 查询
		// Authorization.DOWNLOAD 导出
		// Authorization.UPLOAD 上传
		// Authorization.PUSH 推送
		return true;
	}

	/**
	 * 是否拥有对该接口的增删改权限
     * 此方法可以不重写，则走默认的 boolean allowVisit(MagicUser magicUser, HttpServletRequest request, Authorization authorization) 方法
	 */
	@Override
	public boolean allowVisit(MagicUser magicUser, HttpServletRequest request, Authorization authorization, ApiInfo apiInfo) {
		// Authorization.SAVE 保存
		// Authorization.DELETE 删除
		// Authorization.VIEW 查询
		// 自行写逻辑判断是否拥有如果有，则返回true，反之为false
		return true;
	}

	/**
	 * 是否拥有对该函数的增删改权限
     * 此方法可以不重写，则走默认的 boolean allowVisit(MagicUser magicUser, HttpServletRequest request, Authorization authorization) 方法
	 */
	@Override
	public boolean allowVisit(MagicUser magicUser, HttpServletRequest request, Authorization authorization, FunctionInfo functionInfo) {
		// Authorization.SAVE 保存
		// Authorization.DELETE 删除
		// Authorization.VIEW 查询
		// 自行写逻辑判断是否拥有如果有，则返回true，反之为false
		return true;
	}

	/**
	 * 是否拥有对该分组的增删改权限
     * 此方法可以不重写，则走默认的 boolean allowVisit(MagicUser magicUser, HttpServletRequest request, Authorization authorization) 方法
	 */
	@Override
	public boolean allowVisit(MagicUser magicUser, HttpServletRequest request, Authorization authorization, Group group) {
		// Authorization.SAVE 保存
		// Authorization.DELETE 删除
		// Authorization.VIEW 查询
		// 自行写逻辑判断是否拥有如果有，则返回true，反之为false
		return true;
	}

	/**
	 * 是否拥有对该数据源的增删改权限
     * 此方法可以不重写，则走默认的 boolean allowVisit(MagicUser magicUser, HttpServletRequest request, Authorization authorization) 方法
	 */
	@Override
	public boolean allowVisit(MagicUser magicUser, HttpServletRequest request, Authorization authorization, DataSourceInfo dataSourceInfo) {
		// Authorization.SAVE 保存
		// Authorization.DELETE 删除
		// Authorization.VIEW 查询
		// 自行写逻辑判断是否拥有如果有，则返回true，反之为false
		return true;
	}

}
```