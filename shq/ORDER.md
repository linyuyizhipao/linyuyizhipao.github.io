
# 客户端对接API

##  订单API集合

### 用户订单列表(包括各种条件搜索)

`POST /players/uid_order_list`

####  json结构
```json
{
    "status": 1,
    "msg": "ok",
    "data": {
        "pageCount": 1,
        "pageXXX": 1,
        "pageIndex": 1,
        "pageSize": 2,
        "list": [
            {
                "order_no": "12q1oluw22nrl",
                "booster_status": -1,
                "right_reason": "",
                "big_game_name": "英雄联盟-电信-裁决之地",
                "order_status": 7,
                "order_status_text": "取消订单",
                "is_arb": "0",
                "arb_create_time": "",
                "right_source": -1,
                "booster_amount": 0,
                "id": 245,
                "arb_status": "",
                "amount": 2,
                "search_title": "角色等级 30   英雄数量 139   皮肤数量655   不屈白银Ⅱ   白银框",
                "right_reason_text": "",
                "game_all_name": "英雄联盟-电信-裁决之地",
                "create_time": "2018-07-04 15:25:28",
                "business_no": "xubei",
                "end_time": "2018-07-04 16:35:28",
                "goods_id": 1211221,
                "game_account": "58644405",
                "begin_time": "2018-07-04 15:25:28",
                "foregift_amount": 0,
                "role_name": "浮生",
                "goods_title": "角色等级 30   英雄数量 139   皮肤数量655   不屈白银Ⅱ   白银框",
                "image_path": "//xu-game.xubei.com/game/ZKJHnSeK4Q.png",
                "rights_protection": ""
            }
        ]
    }
}
```
#### 参数说明（登陆码列表）
   |参数|类型|必须|说明|
   |:---|---|---|---|
   | orderStatus| string | 否| 	订单状态：0-未支付，2-支付成功，3-支付失败，4-维权中，5-退款成功，6-退款失败,7-取消订单 ，8-自产自销，100-交易完成 |
   | startTime| string | 是| 查询页数，默认为1 |
   | endTime| string | 是| 开始时间在此时间之后的用户订单 |
   | pageIndex| string | 否| 查询页数，默认为1 |
   | pageSize| string | 否| 查询条数，默认为10 |
   | searchValue| string | 是 | 搜索内容，商品名称/订单编号，就是你订单号搜索的时候用 |

   ### 用户订单详情
   
   `POST /players/uid_order_detail`
   
   ####  json结构
   ```json
{
    "status": 1,
    "msg": "ok",
    "data":
     {
           "actual_amount": 1.1, // 实际付款金额
           "amount": 1.1, // 订单总金额
           "begin_time": "2017-10-24 17:15:52", // 订单租赁开始时间
           "end_time": "2017-10-25 03:25:52", // 订单完成时间
           "foregift_amount": 0, // 订单押金
           "game_all_name": "英雄联盟-网通-德玛西亚", // 游戏区服
           "goods_game": null, // 游戏名称
           "goods_id": 305987, // 商品ID
           "goods_price": 0.1, // 商品时租价格
           "goods_title": "德玛西亚未来战士冠军之刃", // 商品标题
           "id": 1933198, // 订单详情ID
           "image_path": "http://xubei-files.oss-cn-hangzhou.aliyuncs.com/goodsImg/c08bc87e12f24a7b8bbd1656fb0f0603.png", // 订单首页展示图片
           "mobile": "15865133634", // 卖家手机号
           "order_id": 2242678, // 订单ID
           "order_item_price": 1.1, // 订单详情总价格
           "order_no": "0883655215611151D", // 订单号
           "order_status": 0, // 订单状态，0为未支付，1为支付中，2为支付成功，3为支付失败，4维权中，5位退款成功，6位退款失败,7取消订单 ，8自产自销，100 交易完成
           "qq_number": null, // 卖家QQ
           "remark": "重复租赁", // 订单取消原因
           "rent_people": "vmp25d", // 转租人
           "search_title": "德玛西亚未来战士冠军之刃", // 商品描述
           "status_name": "未支付", // 订单状态描述
           "user_name": "15865133634", // 用户名
           "login_device": "pc", // 登录设备，pc/android/iphone
           "game_login_mode": "账号密码登录", // 上号方式："上号器登录","账号密码登录"
           "game_account": "", // 游戏账号
           "game_pwd": "", // 游戏密码
           "goods_code": "123142", // 商品编号
           "create_time": "2017-10-24 17:15:52", // 订单创建时间     
           "role_name": "咖啡不苦" // 角色名
       }
}
   ```
   ####  参数说明
   |参数|类型|必须|说明|
   |:---|---|---|---|
   | orderNo| string | 是| 订单号 |

   ### 用户创建支付前的订单（就是还未进行支付的）
   
  `POST /players/uid_create_order`
   
   ####  json结构
   ```json
   {
       "status": "1",
       "msg": "ok",
       "data": {
           "actual_amount": 2,
           "allnightPrice": 16.8,
           "allow_rank": false,
           "allow_store": false,
           "amount": 2,
           "beforeAmount": 2,
           "before_flag": null,
           "beginTime": "2018-07-02 14:00:31",
           "begin_time": "2018-07-02 14:00:31",
           "big_game_id": 245,
           "big_game_name": "英雄联盟",
           "bindGameId": null,
           "booster_amount": null,
           "booster_order_no": "",
           "booster_status": -1,
           "businessNo": "xubei",
           "businessOrderNo": "",
           "business_no": "xubei",
           "buy_count": "1",
           "buyerId": 1330419,
           "buyerPhone": "18707167919",
           "buyerQq": "",
           "buyer_id": 1330419,
           "buyer_username": "18707167919",
           "buyname": "18707167919",
           "channel_type": null,
           "childOrderCount": 1,
           "compensate": 1,
           "count_down": null,
           "createTime": "2018-07-02 14:00:31",
           "create_time": "2018-07-02 14:00:31",
           "dayPrice": 28.8,
           "endTime": "2018-07-02 15:10:31",
           "end_time": "2018-07-02 15:10:31",
           "exattr1": "xubei_android",
           "exattr2": "1526974863",
           "foregiftAmount": 0,
           "foregift_amount": 0,
           "gameAccount": "58644405",
           "gameAllName": "英雄联盟-电信-裁决之地",
           "gameId": 245,
           "gameNo": "12puc48i8o653",
           "gamePwd": "",
           "game_account": "58644405",
           "game_all_name": "英雄联盟-电信-裁决之地",
           "game_id": 245,
           "game_login_mode": "上号器登录",
           "game_name": "英雄联盟-电信-裁决之地",
           "game_pwd": "",
           "goodActivity": "",
           "goodCode": "8755157014938",
           "goodFee": 0,
           "goodId": 1211221,
           "goodRoleName": "浮生",
           "goodTitle": "角色等级 30   英雄数量 139   皮肤数量655   不屈白银Ⅱ   白银框",
           "goodType": 1,
           "goods_code": "8755157014938",
           "goods_count": 1,
           "goods_game": "英雄联盟",
           "goods_id": 1211221,
           "goods_price": 2,
           "goods_title": "角色等级 30   英雄数量 139   皮肤数量655   不屈白银Ⅱ   白银框",
           "goods_type": 1,
           "hourPrice": 2,
           "id": 5096109691000538391,
           "imagePath": "//xu-game.xubei.com/game/ZKJHnSeK4Q.png",
           "image_path": "//xu-game.xubei.com/game/ZKJHnSeK4Q.png",
           "isChoose": 1,
           "isFinished": 0,
           "isPhone": 0,
           "isShow": null,
           "is_arb": 0,
           "jsqOrder": null,
           "lastOrderLeaseRight": null,
           "login_device": "pc",
           "mobile": "",
           "orderAllAmount": 2,
           "orderBizs": [],
           "orderForegiftAmount": 0,
           "order_id": 5096109691000538391,
           "order_item_price": 2,
           "order_no": "12puc48i8o653",
           "order_price": null,
           "order_status": 0,
           "order_status_text": "待支付",
           "order_status_text2": "",
           "order_text": "租赁成功",
           "phoneType": 0,
           "profitAmount": null,
           "profitExpression": "",
           "qq_number": "",
           "realRefundAmount": null,
           "remark": "",
           "rent_people": "",
           "return_url": "",
           "right_source": -1,
           "role_name": "浮生",
           "salename": "13680330604",
           "search_title": "角色等级 30   英雄数量 139   皮肤数量655   不屈白银Ⅱ   白银框",
           "sellerId": 551570,
           "sellerPhone": "13680330604",
           "sellerQq": "1146508240",
           "seller_id": 551570,
           "shortLease": 2,
           "short_lease": "2",
           "status": 0,
           "status_name": "待支付",
           "type": 1,
           "updateTime": "2018-07-02 14:00:31",
           "user_name": "",
           "weekPrice": 188
       }
   }
   ```
   ####  参数说明
   |参数|类型|必须|说明|
   |:---|---|---|---|
   | goodsId| string | 是| 商品ID |
   | leaseType| string | 是| 租赁类型，1-按小时租，2-按天租，3-按周租，4-通宵畅玩，只有英雄联盟才有后面的2,3,4，其他游戏只有小时,默认为1 |
   | count| string | 是| 商品数量 |

   ### 用户取消订单（非维权的）
   
  `POST /players/cancel_order`
   
   ####  json结构
   ```json
   {
       "status": "1",
       "msg": "ok",
       "data": true //取消成功
   }
   ```
   ####  参数说明
   |参数|类型|必须|说明|
   |:---|---|---|---|
   | orderNo| string | 是| 订单号 |
   | cancelReason| string | 是| 取消原因 |    
   
   
   
   
   
   
   
   ### 用户续租订单
   
  `POST /players/relet`
   
   ####  json结构
```json
{
    "status": "1",
    "msg": "ok",
    "data": {
                    "actual_amount": 1,
                    "allnightPrice": null,
                    "allow_rank": false,
                    "allow_store": false,
                    "amount": 2,
                    "beforeAmount": 2,
                    "before_flag": null,
                    "beginTime": "2018-07-03 16:55:27",
                    "begin_time": "2018-07-03 16:55:27",
                    "big_game_id": 245,
                    "big_game_name": "英雄联盟",
                    "bindGameId": null,
                    "booster_amount": null,
                    "booster_order_no": "",
                    "booster_status": -1,
                    "businessNo": "fenzhan",
                    "businessOrderNo": "",
                    "business_no": "fenzhan",
                    "buy_count": "4",
                    "buyerId": 1330525,
                    "buyerPhone": "13297031693",
                    "buyerQq": "",
                    "buyer_id": 1330525,
                    "buyer_username": "13297031693",
                    "buyname": "13297031693",
                    "channel_type": null,
                    "childOrderCount": 2,
                    "compensate": 1,
                    "count_down": null,
                    "createTime": "2018-07-03 16:55:26",
                    "create_time": "2018-07-03 16:55:26",
                    "dayPrice": null,
                    "endTime": "2018-07-03 19:05:27",
                    "end_time": "2018-07-03 19:05:27",
                    "exattr1": "xubei_android",
                    "exattr2": "1530070528",
                    "foregiftAmount": 0,
                    "foregift_amount": 0,
                    "gameAccount": "555555",
                    "gameAllName": "英雄联盟-电信-卡拉曼达",
                    "gameId": 245,
                    "gameNo": "12pyc6auzrmih",
                    "gamePwd": "",
                    "game_account": "555555",
                    "game_all_name": "英雄联盟-电信-卡拉曼达",
                    "game_id": 245,
                    "game_login_mode": "上号器登录",
                    "game_name": "英雄联盟-电信-卡拉曼达",
                    "game_pwd": "",
                    "goodActivity": "",
                    "goodCode": "76133052528441",
                    "goodFee": 0,
                    "goodId": 2800180,
                    "goodRoleName": "22",
                    "goodTitle": "角色等级 32   英雄数量 32   皮肤数量23   华贵铂金Ⅲ   无段位框",
                    "goodType": 1,
                    "goods_code": "76133052528441",
                    "goods_count": 2,
                    "goods_game": "英雄联盟",
                    "goods_id": 2800180,
                    "goods_price": 1,
                    "goods_title": "角色等级 32   英雄数量 32   皮肤数量23   华贵铂金Ⅲ   无段位框",
                    "goods_type": 1,
                    "hourPrice": 1,
                    "id": 5096516092680209849,
                    "imagePath": "//xu-game.xubei.com/game/ZKJHnSeK4Q.png",
                    "image_path": "//xu-game.xubei.com/game/ZKJHnSeK4Q.png",
                    "isChoose": 1,
                    "isFinished": 0,
                    "isPhone": 0,
                    "isShow": 0,
                    "is_arb": 0,
                    "jsqOrder": null,
                    "lastOrderLeaseRight": null,
                    "login_device": "pc",
                    "mobile": "13297031693",
                    "orderAllAmount": 2,
                    "orderBizs": [],
                    "orderForegiftAmount": 0,
                    "order_id": 5096516092680209849,
                    "order_item_price": 2,
                    "order_no": "12pyc6auzrmih",
                    "order_price": null,
                    "order_status": 2,
                    "order_status_text": "支付成功",
                    "order_status_text2": "",
                    "order_text": "租赁成功",
                    "phoneType": 0,
                    "profitAmount": null,
                    "profitExpression": "",
                    "qq_number": "123456",
                    "realRefundAmount": null,
                    "remark": "",
                    "rent_people": "",
                    "return_url": "",
                    "right_source": -1,
                    "role_name": "22",
                    "salename": "13297031693",
                    "search_title": "角色等级 32   英雄数量 32   皮肤数量23   华贵铂金Ⅲ   无段位框",
                    "sellerId": 1330525,
                    "sellerPhone": "13297031693",
                    "sellerQq": "123456",
                    "seller_id": 1330525,
                    "shortLease": 1,
                    "short_lease": "1",
                    "status": 2,
                    "status_name": "支付成功",
                    "type": 1,
                    "updateTime": "2018-07-03 17:52:51",
                    "user_name": "13297031693",
                    "weekPrice": null
                }
}
   ```
   ####  参数说明
   |参数|类型|必须|说明|
   |:---|---|---|---|
   | count| string | 是| 商品数量 |
   | orderNo| string | 是| 订单号 |

   ### 玩家订单维权
   
  `POST /players/right_protect`
   
   ####  json结构
```json
{
    "status": "1",
    "msg": "ok",
    "data": {
                    "agree": "",
                    "amount": 2,
                    "arbitrate_state": 0,
                    "arbitration_source": 0,
                    "buy_user_Id": 1330525,
                    "buy_user_name": "13297031693",
                    "create_time": "2018-07-03 17:54:09",
                    "deal_create_time": null,
                    "deal_description": "",
                    "deal_result": null,
                    "deal_result_text": "",
                    "detail_create_time": null,
                    "end_time": null,
                    "explains": "",
                    "foregift_amount": 0,
                    "game_name": "英雄联盟-电信-卡拉曼达",
                    "goods_title": "角色等级 32   英雄数量 32   皮肤数量23   华贵铂金Ⅲ   无段位框",
                    "id": 5096530872296017941,
                    "img_id": "",
                    "is_relet": 1,
                    "location": [],
                    "merchant_account": "fenzhan",
                    "order_id": 5096516092680209849,
                    "order_no": "12pyc6auzrmih",
                    "order_pay_time": "2018-07-03 16:55:27",
                    "real_refund_amount": null,
                    "right_no": "12pyc6auzrmih1",
                    "right_reason": 1,
                    "right_reason_text": "账号资料错误/遗漏，无法修改",
                    "rights_protection": "",
                    "sale_user_Id": 1330525,
                    "sale_user_name": "13297031693",
                    "type": 0,
                    "user_Name": "13297031693",
                    "user_id": 0,
                    "user_type": -1,
                    "want_refund_amount": 2
                }
}
   ```
   ####  参数说明
   |参数|类型|必须|说明|
   |:---|---|---|---|
   | orderNo| string | 是| 订单号 |
   | rightReason| string | 是| 维权原因 |
   | rightsProtection| string | 否| 维权说明 |
   | urls| string | 否| 多个维权图片地址，是一个数组 |
   | imgPaths| string | 否| 维权图片地址 |
   | imgId| string | 否| 图片凭证 |

   ### 玩家维权订单的详情
   
  `POST /players/right_protect_order_detail`
   
   ####  json结构
```json
{
    "status": "1",
    "msg": "ok",
    "data": {
                    "agree": "",
                    "amount": 2,
                    "arbitrate_state": 0,
                    "arbitration_source": 0,
                    "buy_user_Id": 1330525,
                    "buy_user_name": "13297031693",
                    "create_time": "2018-07-03 17:54:09",
                    "deal_create_time": null,
                    "deal_description": "",
                    "deal_result": null,
                    "deal_result_text": "",
                    "detail_create_time": null,
                    "end_time": null,
                    "explains": "",
                    "foregift_amount": 0,
                    "game_name": "英雄联盟-电信-卡拉曼达",
                    "goods_title": "角色等级 32   英雄数量 32   皮肤数量23   华贵铂金Ⅲ   无段位框",
                    "id": 5096530872296017941,
                    "img_id": "",
                    "is_relet": 1,
                    "location": [],
                    "merchant_account": "fenzhan",
                    "order_id": 5096516092680209849,
                    "order_no": "12pyc6auzrmih",
                    "order_pay_time": "2018-07-03 16:55:27",
                    "real_refund_amount": null,
                    "right_no": "12pyc6auzrmih1",
                    "right_reason": 1,
                    "right_reason_text": "账号资料错误/遗漏，无法修改",
                    "rights_protection": "",
                    "sale_user_Id": 1330525,
                    "sale_user_name": "13297031693",
                    "type": 0,
                    "user_Name": "13297031693",
                    "user_id": 0,
                    "user_type": -1,
                    "want_refund_amount": 2
                }
}
   ```
   ####  参数说明
   |参数|类型|必须|说明|
   |:---|---|---|---|
   | orderNo| string | 是| 订单号 |

   ### 玩家取消维权订单
   
  `POST /players/cancel_right_protect_order`
   
   ####  json结构
```json
{
    "status": "1",
    "msg": "ok",
    "data": {
                    "agree": "",
                    "amount": 2,
                    "arbitrate_state": 3,
                    "arbitration_source": 0,
                    "buy_user_Id": 1330525,
                    "buy_user_name": "13297031693",
                    "create_time": "2018-07-03 17:54:09",
                    "deal_create_time": null,
                    "deal_description": "",
                    "deal_result": null,
                    "deal_result_text": "",
                    "detail_create_time": null,
                    "end_time": null,
                    "explains": "",
                    "foregift_amount": 0,
                    "game_name": "英雄联盟-电信-卡拉曼达",
                    "goods_title": "角色等级 32   英雄数量 32   皮肤数量23   华贵铂金Ⅲ   无段位框",
                    "id": 5096530872296017941,
                    "img_id": "",
                    "is_relet": 1,
                    "location": [],
                    "merchant_account": "fenzhan",
                    "order_id": 5096516092680209849,
                    "order_no": "12pyc6auzrmih",
                    "order_pay_time": "2018-07-03 16:55:27",
                    "real_refund_amount": null,
                    "right_no": "12pyc6auzrmih1",
                    "right_reason": 1,
                    "right_reason_text": "账号资料错误/遗漏，无法修改",
                    "rights_protection": "",
                    "sale_user_Id": 1330525,
                    "sale_user_name": "13297031693",
                    "type": 0,
                    "user_Name": "13297031693",
                    "user_id": 0,
                    "user_type": -1,
                    "want_refund_amount": 2
                }
}

{
    "status": 0,
    "msg": "维权已经处理,不可以撤销维权",
    "data": false
}

   ```
   ####  参数说明
   |参数|类型|必须|说明|
   |:---|---|---|---|
   | orderNo| string | 是| 订单号 |

   ### 玩家维权上传图片到oss
   
  `POST /players/uploadify_to_oss`
   
   ####  json结构
```json
{
    "status": 1,
    "msg": "success",
    "data": {
        "uploaded": 1,
        "fileName": "shq/201807/10183503915.jpg",
        "url": "img-channel.xubei.com/shq/201807/10183503915.jpg"
    }
}
   ```
   ####  参数说明
   |参数|类型|必须|说明|
   |:---|---|---|---|
   | file| file | 是| 图片 |




