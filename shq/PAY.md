
# 客户端对接API

##  支付API集合

   ### 支付宝支付数据
   
  `POST /players/ali_pay`
   
   ####  json结构
```json
{
    "status": 1,
    "msg": "ok",
    "data": "https://qr.alipay.com/bax02027gamtlord3qlq802f"
}
```
   ####  参数说明 (支付宝支付)
   |参数|类型|必须|说明|
   |:---|---|---|---|
   | orderNo| string | 是| 订单号 |
   | type| string | 是| 支付类型(lease:租赁,topup:充值),默认:lease  |



   ### 微信支付数据
   
  `POST /players/wx_pay`
   
   ####  json结构
   
```json
{
    "status": 1,
    "msg": "ok",
    "data": "weixin://wxpay/bizpayurl?pr=dXs4c2v"
}
```
   
   
   ####  参数说明 (支付宝支付)
   |参数|类型|必须|说明|
   |:---|---|---|---|
   | orderNo| string | 是| 订单号 |
   | type| string | 否| 支付类型(lease:租赁,topup:充值),默认:lease |

   ### 应用内支付行为
   
  `POST /players/app_pay`
   
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
   | orderNo| string | 是| 订单号 |
   | payPwd| string | 是| 支付密码 |

   ### 获取订单支付状态
   
  `POST /players/pay_status`
   
   ####  json结构
   
```json
{
    "status": 1,
    "msg": "ok",
    "data": false   //支付还未成功
}
```
   
   ```json
   {
       "status": 1,
       "msg": "ok",
       "data":  {
                       "actual_amount": 4,
                       "allnightPrice": null,
                       "allow_rank": false,
                       "allow_store": false,
                       "amount": 4,
                       "beforeAmount": 4,
                       "before_flag": null,
                       "beginTime": "2018-07-03 10:26:29",
                       "begin_time": "2018-07-03 10:26:29",
                       "big_game_id": 371,
                       "big_game_name": "地下城与勇士",
                       "bindGameId": null,
                       "booster_amount": null,
                       "booster_order_no": "",
                       "booster_status": -1,
                       "businessNo": "xubei_m",
                       "businessOrderAmount": null,
                       "businessOrderNo": "",
                       "businessUserId": "",
                       "business_no": "xubei_m",
                       "business_userid": "",
                       "buy_count": "0",
                       "buyerId": 1330525,
                       "buyerPhone": "13297031693",
                       "buyerQq": "",
                       "buyer_id": 1330525,
                       "buyer_username": "13297031693",
                       "buyname": "13297031693",
                       "channel_type": null,
                       "childOrderCount": 1,
                       "compensate": 1,
                       "count_down": null,
                       "createTime": "2018-07-03 10:26:29",
                       "create_time": "2018-07-03 10:26:29",
                       "dayPrice": null,
                       "endTime": "2018-07-03 12:36:29",
                       "end_time": "2018-07-03 12:36:29",
                       "exattr1": "xubei_android",
                       "exattr2": "1530070528",
                       "foregiftAmount": 0,
                       "foregift_amount": 0,
                       "gameAccount": "211859685",
                       "gameAllName": "地下城与勇士-北京区-北京1区",
                       "gameId": 371,
                       "gameNo": "12pxdh9v0kxmr",
                       "gamePwd": "",
                       "game_account": "211859685",
                       "game_all_name": "地下城与勇士-北京区-北京1区",
                       "game_id": 371,
                       "game_login_mode": "上号器登录",
                       "game_name": "地下城与勇士-北京区-北京1区",
                       "game_pwd": "",
                       "goodActivity": "",
                       "goodCode": "8928516091977",
                       "goodFee": 0,
                       "goodId": 454075,
                       "goodRoleName": "",
                       "goodTitle": "剑圣-天八流金天空套-强散SS-暗影九瞎子",
                       "goodType": 1,
                       "goods_code": "8928516091977",
                       "goods_count": 2,
                       "goods_game": "地下城与勇士",
                       "goods_id": 454075,
                       "goods_price": 2,
                       "goods_title": "剑圣-天八流金天空套-强散SS-暗影九瞎子",
                       "goods_type": 1,
                       "hourPrice": 2,
                       "id": 5096418213663839043,
                       "imagePath": "//xu-game.xubei.com/game/5FFexrs2mp.png",
                       "image_path": "//xu-game.xubei.com/game/5FFexrs2mp.png",
                       "isChoose": 1,
                       "isFinished": 1,
                       "isPhone": 0,
                       "isShow": null,
                       "is_arb": 0,
                       "jsqOrder": null,
                       "lastOrderLeaseRight": null,
                       "login_device": "pc",
                       "mobile": "",
                       "orderAllAmount": 4,
                       "orderBizs": [],
                       "orderForegiftAmount": 0,
                       "order_id": 5096418213663839043,
                       "order_item_price": 4,
                       "order_no": "12pxdh9v0kxmr",
                       "order_price": null,
                       "order_status": 7,
                       "order_status_text": "取消订单",
                       "order_status_text2": "",
                       "order_text": "租赁成功",
                       "phoneType": 0,
                       "profitAmount": null,
                       "profitExpression": "",
                       "qq_number": "",
                       "realRefundAmount": null,
                       "remark": "订单超时未支付,系统自动取消",
                       "rent_people": "",
                       "return_url": "",
                       "right_source": -1,
                       "role_name": "",
                       "salename": "15753157588",
                       "search_title": "剑圣-天八流金天空套-强散SS-暗影九瞎子",
                       "sellerId": 285160,
                       "sellerPhone": "15753157588",
                       "sellerQq": "757011256",
                       "seller_id": 285160,
                       "shortLease": 2,
                       "short_lease": "2",
                       "status": 7,
                       "status_name": "取消订单",
                       "type": 1,
                       "updateTime": "2018-07-03 10:28:29",
                       "user_name": "",
                       "weekPrice": null
                   }
   }
   ```
   
   
   
   
   ####  参数说明 
   |参数|类型|必须|说明|
   |:---|---|---|---|
   | orderNo| string | 是| 订单号 |


   ### 玩家交易支付列表记录展示
   
  `POST /players/uid_consume_list`
   
   ####  json结构 ×
```json
{
    "status": "1",
    "msg": "ok",
    "data": []
}
```
   
   ####  参数说明 
   |参数|类型|必须|说明|
   |:---|---|---|---|
   | startDate| string | 否| 开始时间 |
   | endDate| string | 否| 截至时间 |
   
   
   
   
   
   
   
   
   
   
   
   
   
   
   ### 找回余额支付密码,设置初始密码
   
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






