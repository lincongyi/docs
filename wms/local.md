### Axios封装

- 请求拦截

1.针对不同的业务模块api，进行过滤，然后添加头部token<br>
2.请求的配置添加cancelToken，取消重复的请求

- 响应拦截

1.针对请求成功后，返回数据进行统一的格式处理<br>
2.针对请求失败后，根据后端返回的状态码，提示用户下一步操作

> 具体细节功能请查看```src/api/client.js```

### Vue-Router

1.本项目没有使用动态路由引入，部分模块需要用到keep-alive缓存路由组件<br>
2.路由守卫```router.beforeEach```，会根据用户进入模块后判断是否具有该模块的权限(针对打印页面不会判断用户权限)

> 具体细节功能请查看```src/router.js```

### VUEX

- ```src/store/index.js```

汇总所有vuex信息

- ```src/store/modules/basicInfo.js```

主要负责记录登录后，用户信息，当前所在仓库信息，用户获取的权限访问菜单等

- ```src/store/modules/buttonPermission.js```

主要负责记录用户每个模块的按钮权限(该模块使用了命名空间)

- ```src/store/modules/reset.js```

初始化加载时根据状态缓存全局state，防止浏览器F5刷新后导致vuex的数据污染

> 具体细节功能请查看```src/store```

### 指令

- ```src/directives```

目前只封装了输入框限制用户输入内容格式的指令，可针对不同的规则配置指令（更多规则可自行添加）。

### 全局通用模块

- ```src/components/global```

主要包含头部、菜单栏、导航栏等

### 通用组件

- ```src/components/common```

抽离出多个模块公用的组件


### webpack配置

- ```vue.config.js```

由于之前用的vue-cli脚手架比较老，不过已经针对项目打包时进行压缩处理，并且可以展示打包图形化信息，日后针对其他更多的模块可进行进一步的优化

```npm run analyze```