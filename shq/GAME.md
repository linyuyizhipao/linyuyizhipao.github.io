
# 客户端对接API

##  游戏API集合

### 游戏列表(包括各种条件搜索)

`POST /players/game_list`

####  json结构
```json
{
    "status": 1,
    "msg": "ok",
    "data": [
        {
            "fzimageurl": "//xu-game.xubei.com/game/xyPPkeNBbS.jpg",
            "game": "英雄联盟",
            "game_id": 245,
            "game_type": 1,
            "id": 1,
            "is_new": 2,
            "path_url": "http://new.xubei.com/shopList.html?gameid=245",
            "search_keys": null,
            "type": 2,
            "url": "//xu-game.xubei.com/game/ZKJHnSeK4Q.png"
        },
        {
            "fzimageurl": "//xu-game.xubei.com/game/HjDMkh6FPY.jpg",
            "game": "绝地求生",
            "game_id": 1494,
            "game_type": 1,
            "id": 7,
            "is_new": 1,
            "path_url": "http://new.xubei.com/shopList.html?gameid=1494",
            "search_keys": null,
            "type": 2,
            "url": "//xu-game.xubei.com/game/QJ7nmczbe4.png"
        }
    ]
}

{
    "status": 1,
    "msg": "ok",
    "data": {
        "j": [
            {
                "fzimageurl": "//xu-game.xubei.com/game/HjDMkh6FPY.jpg",
                "game": "绝地求生",
                "game_id": 1494,
                "game_type": 1,
                "id": 7,
                "is_new": 1,
                "path_url": "http://new.xubei.com/shopList.html?gameid=1494",
                "search_keys": null,
                "type": 2,
                "url": "//xu-game.xubei.com/game/QJ7nmczbe4.png"
            }
        ]
    }
}

```

#### 参数说明
   |参数|类型|必须|说明|
   |:---|---|---|---|
   | type| string|是| 展示游戏列表类型。0：热门游戏；1：端游，2手游,3:首字母|
   | pin| string | 否| 游戏拼音首字母,若type未3时，必需带此参数 |





