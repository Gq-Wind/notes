### vue2

开发插件:暴露一个install 方法,第一个参数为Vue构造器,第二个可选的选项参数.

```vue
MyPlugin.install = function (Vue, options) {
  // 1. 添加全局方法或 property
  Vue.myGlobalMethod = function () {
    // 逻辑...
  }

  // 2. 添加全局资源
  Vue.directive('my-directive', {
    bind (el, binding, vnode, oldVnode) {
      // 逻辑...
    }
    ...
  })

  // 3. 注入组件选项
  Vue.mixin({
    created: function () {
      // 逻辑...
    }
    ...
  })

  // 4. 添加实例方法
  Vue.prototype.$myMethod = function (methodOptions) {
    // 逻辑...
  }
}
```

#### 过滤器：

`{{}}` `v-bind`

全局、局部过滤器

```vue
{{ message | capitalize }}	//message作为参数传到capitalize过滤器中
filters: {
	//局部过滤器
  capitalize: function (value) {
    if (!value) return ''
    value = value.toString()
    return value.charAt(0).toUpperCase() + value.slice(1)
  }
}
//全局
Vue.filter('name',function);
```

