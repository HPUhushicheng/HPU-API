# HPU-API
河南理工大学教务系统api接口分析，一键启动，开箱即用

分析了一波，教务系统网页版涉及到多个加密、混淆等，难度较大，无法直接使用。而移动端无需经过多项验证。
实测只需要获取到token值即可，无需额外的cookie和其他一些不必要参数，代码中已将不必要参数删除。

说明：登录时，需要输入学号和密码，其他参数不需要输入。
获取到的token值，在登录成功后，会自动保存到本地，下次登录时，会自动读取本地token值，无需再次输入。
所有请求返回的响应均为base64编码，需要解码才能使用，不涉及混淆与加密。
# API
1. login.js --> 登录
2. course.js --> 获取课程表
3. score.js --> 获取成绩