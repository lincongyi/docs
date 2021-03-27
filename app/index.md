## 支付h5前端项目

> gitlab地址
http://192.168.50.41/zegopay/dist.git

> 原型图地址
https://www.wulihub.com.cn/go/Qol2gJ/start.html

> UI设计图地址<br>
https://lanhuapp.com/url/YJvpM-x0Dl8<br>
https://app.mockplus.cn/s/eUEXI88bdJK

> Vux(UI框架)
https://doc.vux.li/zh-CN/

## 项目需要注意的细节问题

- ```src/api/mainApi.js```里面有针对各个环境进行打包的地址
- ```src/api/mainApi.js```里面的全局变量Api，记录了请求接口必须的几个参数```fuid/token/Flang```，需要app端提供才能在浏览器正常访问接口
- ```src/userWithdrawal/```这个文件夹里面包含了提现流程的模块，目前该流程主要功能在git的userWithdrawal分支完成
- ```src/utils/common.js```通用的工具函数主要放在这个文件中
- 项目针对zug文字要使用```fontFamily:'myfonts'```的字体格式；针对mm3文字要使用```fontFamily:'myfont'```的字体格式
- 针对部分zug文字乱码问题，还可以使用```uni2zg```方法，具体实现可全局搜索```uni2zg```查看
- 提现时需要创建token和ticket(```Api.createToken``` && ```Api.createTicket```)
- ```scr/store/modules/userWithdrawal.js```里面包含了用户提现的操作记录
- 用户提现流程跑完后，账单查询，后端返回具体状态值查询请全局搜索```formatterState```里面列明了什么值对应什么状态

!> 目前项目需要下载```filezilla```ftp软件，上传到服务器，才可在手机上浏览

- filezilla链接地址：```192.168.50.34:22```


