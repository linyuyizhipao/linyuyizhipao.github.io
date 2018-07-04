
# 客户端对接API

##  玩家API集合

### 玩家登陆

`POST /players/login`

####  json结构
```json
{
    "status": "1",
    "data": true
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
    "data": true
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
    "data": "<img src=\"http://localhost/captcha/flat?SLziFnUy\" >"
}
```
#### 参数说明
   |参数|类型|必须|说明|
   |:---|---|---|---|

### 忘记密码

`POST /players/forgetpassWord`

####  json结构
```json
{
    "status": 1,
    "data": "找回密码成功"
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
    "status": 1,
    "data": "退出成功"
}
```
#### 参数说明
   |参数|类型|必须|说明|
   |:---|---|---|---|


### 获取短信验证码

`POST /players/logout`

####  json结构
```json
{
    "status": 1,
    "data": "短信发送成功"
}
```
#### 参数说明
   |参数|类型|必须|说明|
   |:---|---|---|---|
   | mobile| string|是|手机号码 |
   | captcha| string | 是| 图形验证码 |





