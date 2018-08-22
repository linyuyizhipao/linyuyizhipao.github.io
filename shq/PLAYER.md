
# 客户端对接API

##  玩家API集合

### 玩家登陆

`POST /players/login`

####  json结构
```json
{
    "status": 1,
    "msg": "登陆成功",
    "data": {
        "userId": "2e22d449-95ca-4533-a3c1-940e04a544ef"
        "url": "http://...."
    }
}

{
    "status": 0,
    "msg": "登陆失败,密码错误",
    "data": []
}
```
#### 参数说明
   |参数|类型|必须|说明|
   |:---|---|---|---|
   | mobile| string|是|手机号码 |
   | pwd| string | 是| 密码 |

### 玩家注册

`POST /players/register`

####  json结构
```json
{
    "status": "1",
    "msg" : "注册成功",
    "data": {"url":"http://www."}
}

{
    "status": 0,
    "msg": "图形验证码错误",
    "data": []
}
```
#### 参数说明
   |参数|类型|必须|说明|
   |:---|---|---|---|
   | mobile| string|是|手机号码 |
   | pwd| string | 是| 密码 |
   | code| string | 是| 短信验证码 |

### 刷新验证码(非手机短信验证码)

`GET /captcha`

#### 参数说明
   |参数|类型|必须|说明|
   |:---|---|---|---|

### 忘记密码

`POST /players/forget_pwd`

####  json结构
```json
{
    "status": 1,
    "msg": "找回密码成功",
    "data": [{"url":"http://www."}]
}

{
    "status": 0,
    "msg": "图形验证码错误",
    "data": []
}

```
#### 参数说明
   |参数|类型|必须|说明|
   |:---|---|---|---|
   
   
   
### 记住密码

`POST /players/rememberpwd`

####  json结构
```json
{
    "status": 1,
    "msg": "ok",
    "data": {}
}

{
    "status": 0,
    "msg": "图形验证码错误",
    "data": []
}

```
#### 参数说明
   |参数|类型|必须|说明|
   |:---|---|---|---|


### 退出登陆

`POST /players/logout`

####  json结构
```json
{
    "status": 0,
    "msg": "ok",
    "data": "退出成功"
}
```
#### 参数说明
   |参数|类型|必须|说明|
   |:---|---|---|---|


### 获取短信验证码

`POST /players/sms_verify_code`

####  json结构
```json
{
    "status": 1,
    "msg": "短信发送成功",
    "data": []
}

{
    "status": 0,
    "msg": "参数错误",
    "data": "验证码错误"
}

```
#### 参数说明
   |参数|类型|必须|说明|
   |:---|---|---|---|
   | mobile| string|是|手机号码 |
   | captcha| string | 是| 图形验证码 |
   
   
   
   
   
### 获取banner信息

`POST /players/show_banner`

####  json结构
```json
{
    "status": 1,
    "msg": "ok",
    "data": {
        "current_page": 1,
        "data": [
            {
                "id": 37,
                "banner_name_id": 5,
                "img_url": "img-channel.xubei.com/shq/201807/12182424962.jpg",
                "location": "23",
                "sort": 2,
                "title": "发射点发大水",
                "desc": "3434563456",
                "create_at": "1531391067",
                "status": 1
            },
            {
                "id": 36,
                "banner_name_id": 5,
                "img_url": "img-channel.xubei.com/shq/201807/12181535597.jpg",
                "location": "4234234243",
                "sort": 3,
                "title": "0",
                "desc": "23464565475687856815345634654",
                "create_at": "1531390545",
                "status": 1
            },
            {
                "id": 33,
                "banner_name_id": 5,
                "img_url": "img-channel.xubei.com/shq/201807/12162719536.jpg",
                "location": "q234000000000000000",
                "sort": 234,
                "title": "0",
                "desc": "54564",
                "create_at": "1531384043",
                "status": 1
            },
            {
                "id": 32,
                "banner_name_id": 5,
                "img_url": "img-channel.xubei.com/shq/201807/12163833566.jpg",
                "location": "q234111",
                "sort": 2341111,
                "title": "0",
                "desc": "54564111",
                "create_at": "1531384027",
                "status": 1
            }
        ],
        "first_page_url": "http://localhost/players/show_banner/5?page=1",
        "from": 1,
        "next_page_url": null,
        "path": "http://localhost/players/show_banner/5",
        "per_page": 15,
        "prev_page_url": null,
        "to": 4
    }
}

```
#### 参数说明
   |参数|类型|必须|说明|
   |:---|---|---|---|
   | type| string|是|banner类型.1:热门推荐;2.轮播图;3:一元专区;4新游飙升榜;5:热门租单|

