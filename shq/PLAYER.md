
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
    "data": [
        {
            "id": 31,
            "banner_name_id": 4,
            "img_url": "img-channel.xubei.com/shq/201807/12132214863.jpg",
            "location": "点击跳转的http链接",
            "sort": 3,
            "desc": "显示影藏的内容",
            "create_at": "1531372940",
            "status": 1
        }
    ]
}

```
#### 参数说明
   |参数|类型|必须|说明|
   |:---|---|---|---|
   | type| string|是|banner类型.1:热门推荐;2.轮播图;3:一元专区;4新游飙升榜;5:热门租单|





