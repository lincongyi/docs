## 地址

> gitlab地址
http://192.168.50.41//lincongyi/risk-admin-web.git

> 测试环境地址
http://192.168.50.69:8013/

> 预发布环境地址
http://192.168.1.106:8013/

> 开发文档api
http://192.168.50.69:3000/

> 原型图地址
https://www.wulihub.com.cn/go/WElA8j/start.html (密码：fk123456)

> 构建生产环境
```npm run build:prod || npm run build```

> 构建预发布环境
```npm run build:pretest```

## 菜单模块划分

- 规则管理  rule
  - 风险规则  risk
  - 额度规则  quota
  - 白名单管理  whiteList
  - 黑名单管理  blackList

- 日志管理  log
  - 风控日志  riskLog

- 人工介入审核  examine
  - 人工介入  intervention

- 配置管理  configure
  - 系统配置  system
  - 风控定时任务  timing