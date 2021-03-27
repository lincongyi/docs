### Axios封装

1.封装请求头（请求拦截）<br>
2.根据后端返回请求状态进行下一步操作（响应拦截）

### api接口整合

- 所有模块api接口都放在```src/api/```文件夹中，文件夹命名对应项目模块命名

### Vue-Router

-  ```router.beforeEach```路由守卫中采用```loadMenus```方法动态引入路由模块

### VUEX

- ```src/store/index.js```

汇总所有vuex信息；使用webpack的```require.context()```方法遍历```modules```文件夹统一引入所有模块

- ```src/store/permission.js```

主要负责记录用户权限

- ```src/store/user.js```

主要负责记录用户权限

!> 这两个state模块需要关注下

### 全局通用模块

- ```src/components/layout/```

主要包含头部、菜单栏、导航栏、工具栏等

### 数据字典

项目使用到数据字典，在使用```main.js```中```vue.use(dict)```注册了全局组件<br>
> 具体细节功能请查看```src/components/Dict/Dict.js```

### CRUD（增删查改）

项目已为各个模块统一封装了CRUD方法，可以针对性的启用禁用某个功能；<br>
里面的方法有点多，可根据具体需求酌情研究
> 具体细节功能请查看```src/components/Crud/```文件夹

### 其他模块细节

1.```src/utils/auth.js```用户登录后token信息会保存在浏览器的cookies里面，该js文件提供了```get/set/remove```方法操作token<br>
2.```src/utils/validate.js```封装了部分表单验证方法<br>
3.```src/components/Echarts/```文件夹中封装了各种可使用的图表<br>
4.```src/components/Permission/```按钮权限指令

