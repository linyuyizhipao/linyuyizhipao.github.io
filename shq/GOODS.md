
# 客户端对接API

##  商品API集合

   ### 商品列表
   
  `POST /goods/goods_list`
   
   ####  json结构
```json
{
    "status": 1,
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
            },
            {
                "big_game_name": "英雄联盟",
                "compensate": 1,
                "cutis_num": 30,
                "foregift": 0,
                "game_all_name": "英雄联盟-电信-卡拉曼达",
                "game_name": "卡拉曼达",
                "goods_id": 1771567,
                "goods_status": 3,
                "goods_title": "角色等级 30   英雄数量 130   皮肤数量30   英勇黄铜Ⅳ   黄铜框",
                "grading_id": "yyht1",
                "grading_name": "英勇黄铜Ⅳ",
                "hero_num": 130,
                "id": 1771567,
                "if_play_qualifying": "支持",
                "lease_price": "1.00",
                "role_name": "jfrsf",
                "search_title": "8488满英雄 全英雄 皮肤 100 各种限定皮肤 钻石头像 号上妹子好友多 装逼神器 ",
                "short_lease": 3,
                "status_name": "展示中",
                "success_rent_num": 50,
                "actity": null,
                "buy_count": 4,
                "fzimageurl": "//xu-game.xubei.com/game/xyPPkeNBbS.jpg",
                "game_id": 245,
                "hot_value": 264,
                "imageurl": "//xu-game.xubei.com/game/ZKJHnSeK4Q.png",
                "is_phone": 0,
                "is_show": null,
                "phone_type": 3,
                "signseller": 1,
                "stickorder": 0,
                "user_id": 459793,
                "user_order": 0
            },
            {
                "big_game_name": "英雄联盟",
                "compensate": 1,
                "cutis_num": 318,
                "foregift": 0,
                "game_all_name": "英雄联盟-网通-弗雷尔卓德",
                "game_name": "弗雷尔卓德",
                "goods_id": 1837185,
                "goods_status": 3,
                "goods_title": "角色等级 30   英雄数量 140   皮肤数量318   无段位   无段位框",
                "grading_id": "wdw",
                "grading_name": "无段位",
                "hero_num": 140,
                "id": 1837185,
                "if_play_qualifying": "支持",
                "lease_price": "2.00",
                "role_name": "小鲨鱼丶 conor",
                "search_title": "3160 角色等级30 全英雄 皮肤314 龙瞎等各种限定",
                "short_lease": 3,
                "status_name": "展示中",
                "success_rent_num": 14,
                "actity": null,
                "buy_count": 3,
                "fzimageurl": "//xu-game.xubei.com/game/xyPPkeNBbS.jpg",
                "game_id": 245,
                "hot_value": 248,
                "imageurl": "//xu-game.xubei.com/game/ZKJHnSeK4Q.png",
                "is_phone": 0,
                "is_show": null,
                "phone_type": 3,
                "signseller": 1,
                "stickorder": 0,
                "user_id": 459793,
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

   ####  参数说明 (商品名称搜索)
   |参数|类型|必须|说明|
   |:---|---|---|---|
   | pageIndex| string | 是| 当前第几页，从1开始 |
   | pageSize| string | 是| 一页显示的条数 |
   | bigGameName| string | 是|区服名称 |
   | businessNo| string | 是| 商户号 |
   | listType| string | 是| 商品列表类型。商品名称搜索类型为 0：商品名称搜索；1：热门商品；2：推荐商品；3：用户收藏商品；4：价格区间；5：商品区服；6：是否充值；7：是否签约；8:价格倒序；9：时间倒序；10:综合排序 |
   | server| string | 是| 游戏名称 |

   ####  参数说明 (1元起，2元起，3元起)
   |参数|类型|必须|说明|
   |:---|---|---|---|
   | pageIndex| string | 是| 当前第几页，从1开始 |
   | pageSize| string | 是| 一页显示的条数 |
   | bigGameName| string | 是|区服名称 |
   | businessNo| string | 是| 商户号 |
   | listType| string | 是| 商品列表类型。商品名称搜索类型为 0：商品名称搜索；1：热门商品；2：推荐商品；3：用户收藏商品；4：价格区间；5：商品区服；6：是否充值；7：是否签约；8:价格倒序；9：时间倒序；10:综合排序 |
   | priceRange| string | 是| 起步价 |
   
   ####  参数说明 (商品区服大厅等刷选)
   |参数|类型|必须|说明|
   |:---|---|---|---|
   | pageIndex| string | 是| 当前第几页，从1开始 |
   | pageSize| string | 是| 一页显示的条数 |
   | bigGameName| string | 是|区服名称 |
   | businessNo| string | 是| 商户号 |
   | listType| string | 是| 商品列表类型。商品名称搜索类型为 0：商品名称搜索；1：热门商品；2：推荐商品；3：用户收藏商品；4：价格区间；5：商品区服；6：是否充值；7：是否签约；8:价格倒序；9：时间倒序；10:综合排序 |
   | gameName| string | 是| 游戏区服,选择的区服以-隔开  例如: 英雄联盟-网通-德玛西亚  |
   
   ####  参数说明 (商品是否押金)
   |参数|类型|必须|说明|
   |:---|---|---|---|
   | pageIndex| string | 是| 当前第几页，从1开始 |
   | pageSize| string | 是| 一页显示的条数 |
   | bigGameName| string | 是|区服名称 |
   | businessNo| string | 是| 商户号 |
   | listType| string | 是| 商品列表类型。商品名称搜索类型为 0：商品名称搜索；1：热门商品；2：推荐商品；3：用户收藏商品；4：价格区间；5：商品区服；6：是否充值；7：是否签约；8:价格倒序；9：时间倒序；10:综合排序 |
   | deposit| string | 是| 押金（1-有，0-无） |
   

   ####  参数说明 (商品是否签约)
   |参数|类型|必须|说明|
   |:---|---|---|---|
   | pageIndex| string | 是| 当前第几页，从1开始 |
   | pageSize| string | 是| 一页显示的条数 |
   | bigGameName| string | 是|区服名称 |
   | businessNo| string | 是| 商户号 |
   | listType| string | 是| 商品列表类型。商品名称搜索类型为 0：商品名称搜索；1：热门商品；2：推荐商品；3：用户收藏商品；4：价格区间；5：商品区服；6：是否充值；7：是否签约；8:价格倒序；9：时间倒序；10:综合排序 |
   | signSeller| string | 是| 签约卖家（1-是，0-否） |
   






   ### 玩家收藏商品(若是已收藏的商品，则为取消收藏行为)
   
  `POST /goods/uid_collect_goods`
   
   ####  json结构 （收藏）
```json
{
    "status": 1,
    "data": "收藏成功"
}
```
   ####  json结构（取消收藏）
```json
{
    "status": 1,
    "data": "取消成功"
}
```
   ####  参数说明
   |参数|类型|必须|说明|
   |:---|---|---|---|
   | goodsId| string | 是| 订单编号 |






