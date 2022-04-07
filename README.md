# SYSU Health Report Template

[SYSU Health Report](https://github.com/Syderny/SYSU-HealthReport) 的配置模板。
原项目为 [@Editst](https://github.com/Editst) 的 [jksb_sysu](https://github.com/Editst/SYSU-HealthReport) 。本项目更改了验证码的识别方式，现在使用百度ai提供的免费应用，更加方便使用。

**已可以正常运行，仍存在较大不确定性，谨慎使用**

# 使用

- 点击 [Use this template](https://github.com/Syderny/AutoHealthReport/generate) 创建一个新的仓库。

- 注册 [百度云账号](https://ai.baidu.com/tech/ocr) ，并创建一个自己的文字识别应用（注意包括通用文字识别（标准版）API），保存App ID、Api Key、Secret Key这三个参数。

<img width="787" alt="image" src="https://user-images.githubusercontent.com/43570957/159112921-eded6820-fc06-4ab3-a6ab-d951f8af22c6.png">


- 在新仓库中 Settings-Secrets-Action 添加以下secrets（Repository Secrets即可），根据自己的netid账号密码，以及刚刚获取的三个参数。

![image](https://user-images.githubusercontent.com/43570957/159113007-d0b9f250-b087-4b57-b8d3-de0445d84078.png)

![image](https://user-images.githubusercontent.com/43570957/159113021-3d90d369-5a5a-4d6c-937d-72927fea65af.png)

配置完毕。

# 定时运行

默认配置为每天 23:30 UTC 运行，对应运行时间约为 7:30 Asia/Shanghai（实际上在7：40），如需修改时间请参考[这里](https://docs.github.com/en/actions/learn-github-actions/events-that-trigger-workflows#scheduled-events)。

# 手动运行
用于测试是否可行，点击仓库的Actions
<img width="930" alt="image" src="https://user-images.githubusercontent.com/43570957/159113130-bf787f41-167f-431b-8471-2616feb1bf81.png">
可查看后台运行的命令行，运行成功可在微信收到申报成功的通知。

# 可选

## Telegram Bot 推送

如果希望使用 Telegram Bot 推送运行结果，将你的 Bot 的 Token 填入 `TG_BOT_TOKEN`，将你与该 Bot 的 chat_id 填入 `TG_CHATID` 中。

具体操作可以参考[官方文档](https://core.telegram.org/bots/api#sendmessage)，其中 `chat_id` 的可以使用 `getUpdates` 方法或者问候 [@userinfobot](https://t.me/userinfobot) 获得。

使用该通知方式假定你已知道如何设置，其他问题请 Google，否则请放弃。

## Server 酱推送

如果希望使用 server 酱推送运行结果，将你的 wxsend_key 填入 `TG_BOT_TOKEN` 中，具体获取方式可前往[官网](https://sct.ftqq.com/)查看。

# TODO

**欢迎提交 pr 来增加其他通知推送方式。**

# 免责声明

此脚本仅供学习交流，禁止商业使用，使用软件过程中，发生意外造成的损失由使用者承担。如遇身体不适、或居住地址发生变化，请及时更新健康申报信息。
