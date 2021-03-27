### Axios封装

- 请求拦截

1.请求的配置添加cancelToken，取消重复的请求
2.云端请求接口无需带token，只需要带上withCredentials凭证即可(withCredentials = true)

- 响应拦截

1.针对请求成功后，返回数据进行统一的格式处理<br>
2.针对请求失败后，根据后端返回的状态码，提示用户下一步操作

> 具体细节功能请查看```src/api/client.js```

### Vue-Router

1.本项目没有使用动态路由引入，部分模块需要用到keep-alive缓存路由组件

> 具体细节功能请查看```src/router.js```

### VUEX

- ```src/store/index.js```

汇总所有vuex信息

- ```src/store/modules/basicInfo.js```

主要负责记录登录后，用户信息，当前所在仓库信息，用户获取的权限访问菜单等

- ```src/store/modules/reset.js```

初始化加载时根据状态缓存全局state，防止浏览器F5刷新后导致vuex的数据污染

> 具体细节功能请查看```src/store```

### 指令

- ```src/directives```

目前只封装了输入框限制用户输入内容格式的指令，可针对不同的规则配置指令（更多规则可自行添加）。

### 全局通用模块

- ```src/components/global```

主要包含头部、菜单栏、导航栏等

### 展示配置的按钮权限页面 menuButtonList

- ```src/business/menuButtonList.vue```

为每个按钮配置权限的展示页面。<br>
在菜单页面配置了按钮权限后，请在menuButtonList.vue手动添加按钮参数，方便后端开发人员根据前端配置的按钮参数进行对应的处理<br>
该页面可直接访问