## 「e家宜业」物联网服务端

> 物联网硬件对接没有统一标准，此部分仅作参考，有能力的同学和企业可自行拆分、对接开发。

### 智能门禁

> 目前仅支持卡帕斯品牌

#### 接口地址

- 心跳检测 `域名/iot/entrance?id={{接口形参第一位}}&community_id={{接口形参第二位}}&method=status`
- 开门刷卡 `域名/iot/entrance?id={{接口形参第一位}}&community_id={{接口形参第二位}}&method=access`

#### 门禁配置

* 选择`启用AES128加密`，秘钥配置中台对应的秘钥
* 心跳间隔设置为`60`
* `本机信息-标识`配置为中台对应的标识名称
* `通讯协议`选择`启用Http通讯`
* `验证模式`选择`脱机验证优先`（主要针对老旧小区用的RFID卡）
