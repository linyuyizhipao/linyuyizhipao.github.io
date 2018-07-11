
# 客户端对接API

##  支付API集合

   ### 用户订单支付
   
  `POST /players/uid_pay_data`
   
   ####  json结构
   ####（微信支付返回）
```json
{
"status": "1",
"msg": "ok",
"data": "https://statecheck.swiftpass.cn/pay/wappay?token_id=28035c4e421a571ed7e18e0cb4f27de84&service=pay.weixin.wappayv2"
}
```
   ####（支付宝支付返回）

```json
{
    "status": "1",
    "msg": "ok",
    "data": {
        "paramStr": "alipay_sdk=alipay-sdk-java-dynamicVersionNo&app_id=2018020602151130&biz_content=%7B%22body%22%3A%22%E8%99%9A%E8%B4%9D%E8%AE%A2%E5%8D%95-%E8%B4%A6%E5%8F%B7%E7%A7%9F%E8%B5%81-72da8de89771%22%2C%22out_trade_no%22%3A%2272da8de89771%22%2C%22product_code%22%3A%22QUICK_MSECURITY_PAY%22%2C%22subject%22%3A%22%22%2C%22timeout_express%22%3A%2230m%22%2C%22total_amount%22%3A%220.01%22%7D&charset=utf-8&format=json&method=alipay.trade.app.pay&notify_url=http%3A%2F%2F106.15.103.137%2Fzycartrade-app%2Fpay%2FnoticeByWechat&sign=Eoo6VZs8P6NOSPIYd4HkJN%2FgA76OCaz8r%2FW8SkY%2FbSGPBCyHM6TTQXkLLZcTrlCy0N4lXpQ9%2BTf%2Fyye8x3H6Rgn%2FQ1oT9a%2FyR4gYbxkpvWyMP9jvjzkt6KT5xfA26grEZkrBjrQu9kdUT0WRPBhzMgmyOGyzslvEBCzEmYIVxBn%2FUJ3vlGyfZki1xGiK74LgXRNYhWWqndtDA959Bw9inVjl88qrR%2F4ahCMkAwINBl2zzibA%2BSWbSdDAXs%2FabGUmrT2GaMpXvY1ttNWj%2FLVmZWFL0moLt8DNQVpPLb42wE5zaT5KLTZQkfLWS8UfjFdOiDfgxXg3UnwYrWXrp6ZJug%3D%3D&sign_type=RSA2&timestamp=2018-03-12+16%3A06%3A42&version=1.0"
    }
}
```
   ####（余额支付返回）
```json
{
    "status": "1",
    "msg": "ok",
    "data": true
}
```
   
   ####  参数说明 (支付宝支付)
   |参数|类型|必须|说明|
   |:---|---|---|---|
   | pay_type| string | 是| 支付类型 |
   | orderNo| string | 是| 订单号 |
   | type| string | 是| 支付类型(lease:租赁,topup:充值) |

   ####  参数说明 (微信支付)
   |参数|类型|必须|说明|
   |:---|---|---|---|
   | pay_type| string | 是| 支付类型 |
   | orderNo| string | 是| 订单号 |
   | type| string | 是| 支付类型(lease:租赁,topup:充值) |

   ####  参数说明 (余额支付)
   |参数|类型|必须|说明|
   |:---|---|---|---|
   | pay_type| string | 是| 支付类型 |
   | payPwd| string | 是| 支付密码 |
   | orderNo| string | 是| 订单号 |
   | businessNo| string | 是| 商户号 |

   ### 玩家交易支付列表记录展示
   
  `POST /players/uid_consume_list`
   
   ####  json结构 ×
```json
{
    "status": "1",
    "msg": "ok",
    "data": true
}
```
   
   ####  参数说明 
   |参数|类型|必须|说明|
   |:---|---|---|---|
   | pageIndex| string | 否| 当前页 |
   | pageSize| string | 否| 页面大小 |
   | startDate| string | 否| 开始时间 |
   | endDate| string | 否| 截至时间 |
   
   
   
   
   
   ### 找回余额支付密码
   
  `POST /players/foundPayPwd`
   
   ####  json结构 
```json
{
    "status": "1",
    "msg": "ok",
    "data": true
}
```
   
   ####  参数说明 
   |参数|类型|必须|说明|
   |:---|---|---|---|
   | code| string | 是| 验证码 |
   | newPassword| string | 是| 新密码 |






