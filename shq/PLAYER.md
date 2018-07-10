
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
   | mobile| string|是|手机号码 |
   | pwd| string | 是| 密码 |
   | code| string | 是| 短信验证码 |

### 刷新验证码(非手机短信验证码)

`POST /players/refreshCaptcha`

####  json结构
```json
{
    "status": 1,
    "msg": "success",
    "data": "<img src=\"http://localhost/captcha/flat?XBtwjNFc\" >"
}
```
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


### 退出登陆

`POST /players/logout`

####  json结构
```json
{
    "status": 0,
    "msg": "success",
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





