
# 客户端对接API

##  游戏API集合

### 游戏列表(包括各种条件搜索)

`POST /players/uid_order_list`

####  json结构
```json
{
    "status": "1",
    "data": {
        "list": [
            {
                "actual_amount": 1.1, // 实际付款金额
                "amount": 1.1, // 订单总金额
                "begin_time": "2017-10-24 17:15:52", // 订单租赁开始时间
                "end_time": "2017-10-25 03:25:52", // 订单完成时间
                "foregift_amount": 0, // 订单押金
                "game_all_name": "英雄联盟-网通-德玛西亚", // 游戏区服
                "goods_game": null, // 游戏名称
                "goods_id": 305987, // 商品ID
                "goods_price": 0.1, // 商品价格
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
                "role_name": "角色名" // 角色名
            }
        ],
        "pageCount": 12, // 查询总条数
        "pageNumber": 12, // 查询分页
        "pageIndex": 1,
        "pageSize": 10
    }
}
```

#### 参数说明（热门游戏）
   |参数|类型|必须|说明|
   |:---|---|---|---|
   | type| string|是| 展示游戏列表类型。0：热门游戏；1：端游，2手游,3:首字母|
   
   
#### 参数说明（端游）
   |参数|类型|必须|说明|
   |:---|---|---|---|
   | type| string|是| 展示游戏列表类型。0：热门游戏；1：端游，2手游,3:首字母|
   
   
#### 参数说明（手游）
   |参数|类型|必须|说明|
   |:---|---|---|---|
   | type| string|是| 展示游戏列表类型。0：热门游戏；1：端游，2手游,3:首字母|

#### 参数说明（首字母）
   |参数|类型|必须|说明|
   |:---|---|---|---|
   | type| string|是| 展示游戏列表类型。0：热门游戏；1：端游，2手游,3:首字母|
   | pin| string | 是| 游戏拼音首字母 |





