
# 客户端对接API

##  商品API集合

   ### 商品列表
   
  `POST /goods/goods_list`
   
   ####  json结构
```json
{
    "status": 1,
    "msg": "ok",
    "data": {
        "list": [
            {
                "big_game_name": "英雄联盟",
                "compensate": 0,
                "cutis_num": 655,
                "foregift": 0,
                "game_all_name": "英雄联盟-电信-裁决之地",
                "game_name": "裁决之地",
                "goods_id": 1211221,
                "goods_status": 3,
                "goods_title": "角色等级 30   英雄数量 139   皮肤数量655   不屈白银Ⅱ   白银框",
                "grading_id": "bqby3",
                "grading_name": "不屈白银Ⅱ",
                "hero_num": 139,
                "id": 1211221,
                "if_play_qualifying": "支持",
                "lease_price": "2.00",
                "role_name": "浮生",
                "search_title": "你直“139全部英雄655皮肤，狗年龙年全套摄魂使者恐惧新星斩星魔摄魂VN 创战纪希维尔 龙虾 JS",
                "short_lease": 2,
                "status_name": "展示中",
                "success_rent_num": 153,
                "actity": null,
                "buy_count": 2,
                "fzimageurl": "//xu-game.xubei.com/game/xyPPkeNBbS.jpg",
                "game_id": 245,
                "hot_value": 1532,
                "imageurl": "//xu-game.xubei.com/game/ZKJHnSeK4Q.png",
                "is_phone": 0,
                "is_show": null,
                "phone_type": 3,
                "signseller": 1,
                "stickorder": 0,
                "user_id": 551570,
                "user_order": 0
            }
        ],
        "pagecount": 5381,
        "pageindex": 1,
        "pagesize": 20,
        "total": 5381,
        "totalpagenum": 270
    }
}
```

   ####  参数说明 
   |参数|类型|必须|说明|
   |:---|---|---|---|
   | pageIndex| string | 否| 当前第几页，从1开始 |
   | pageSize| string | 否| 一页显示的条数 |
   | bigGameName| string | 否|区服名称 |
   | businessNo| string | 否| 商户号 |
   | server| string | 否| 游戏名称 |
   | priceRange| string | 否| 起步价 |
   | gameName| string | 否| 游戏区服,选择的区服以-隔开  例如: 英雄联盟-网通-德玛西亚  |
   | deposit| string | 否| 押金（1-有，0-无） |
   | signSeller| string | 否| 签约卖家（1-是，0-否） |
   
   
   ### 商品详情
   
  `POST /goods/goods_detail`
   
   ####  json结构
```json
{
    "status": 1,
    "msg": "ok",
    "data": {
        "detail": {
            "allnight_play": 18,
            "all_night_play": 18,
            "big_game_id": 245,
            "big_game_name": "英雄联盟",
            "compensate": 1,
            "coupon": 12,
            "cutis_num": 318,
            "day_lease": 40,
            "foregift": 0,
            "game_account": "********",
            "game_all_name": "英雄联盟-网通-弗雷尔卓德",
            "game_id": 269,
            "game_name": "弗雷尔卓德",
            "game_pwd": "********",
            "gold_coins": 12321,
            "goods_code": "9945979313009",
            "goods_flag": 0,
            "goods_status": 3,
            "goods_title": "3160 角色等级30 全英雄 皮肤314 龙瞎等各种限定",
            "grade_id": 30,
            "grading_frame_id": 0,
            "grading_id": "wdw",
            "grading_name": "无段位",
            "hero_num": 140,
            "hour_lease": 2,
            "id": 1837185,
            "if_play_qualifying": 0,
            "lease_price": 2,
            "remark": "角色等级30&nbsp;全英雄&nbsp;皮肤314&nbsp;龙瞎等各种限定角色等级30&nbsp;全英雄&nbsp;皮肤314&nbsp;龙瞎等各种限定角色等级30&nbsp;全英雄&nbsp;皮肤314&nbsp;龙瞎等各种限定角色等级30&nbsp;全英雄&nbsp;皮肤314&nbsp;龙瞎等各种限定角色等级30&nbsp;全英雄&nbsp;皮肤314&nbsp;龙瞎等各种限定",
            "role_name": "小鲨鱼丶 conor",
            "rune_stones": 5,
            "search_title": "角色等级 30   英雄数量 140   皮肤数量318   无段位   无段位框",
            "server_id": 12,
            "server_name": "账号出租",
            "short_lease": 3,
            "user_id": 459793,
            "week_lease": 150,
            "actity": null,
            "actity_str": null,
            "business_no": "xubei",
            "buy_count": 3,
            "day_hours": null,
            "ddaylease": 40,
            "isme": "1",
            "is_phone": 0,
            "is_show": null,
            "is_show_text": "上号器登录",
            "linghuozupai_id": 1,
            "phone": "18268373736",
            "phone_type": 0,
            "phone_type_text": "安卓",
            "qq": "1143854041",
            "signseller": 1,
            "ten_hours": null,
            "wweeklease": null
        },
        "picture": [
            {
                "location": "http://files.xubei.com/goodsImg/5f709d7f6b1b4a00ad5fb51f478dc6c8.jpg"
            }
        ]
    }
}
```
 
   ####  参数说明
   |参数|类型|必须|说明|
   |:---|---|---|---|
   | goodsId| string | 是| 商品ID |
   
   
   
   
   
### 用户收藏列表

`POST /players/uid_goods_collect_lists`

####  json结构
```json

```
#### 参数说明
   |参数|类型|必须|说明|
   |:---|---|---|---|


   ### 玩家收藏商品(若是已收藏的商品，则为取消收藏行为)
   
  `POST /goods/uid_collect_goods`
   
   ####  json结构 （收藏）
```json
{
    "status": 1,
    "msg": "收藏成功",
    "data": []
}
```
   ####  json结构（取消收藏）
```json
{
    "status": 1,
    "msg": "取消成功",
    "data": []
}
```
   ####  参数说明
   |参数|类型|必须|说明|
   |:---|---|---|---|
   | goodsId| string | 是| 商品ID |







