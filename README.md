
# 小程序应用活动API

##  H5页面使用

#### 根据活动id获取活动页面信息

#### 汇总参数 方法

`POST /v4/activity/act-get-info`

####  json结构

```json
    {
       "errno": 0,
       "errmsg":"请求成功",
       "data": {
                "act_id": "3",   //活动id
                "act_home_style": "1",  //活动风格，每一种风格只能确认活动页面的显示风格，并不确认其他信息，比如说是否发短息。
                "act_home_page": "images/activityImages/templateHome_3.png",  //参与活动的页面背景图片
                "act_home_title": "234423",  //活动参与页面标题
                "act_home_rules": "[\"53465\"]",//活动参与页面的规则显示
                "act_success_title": "234", //活动成功后的跳转页面的标题
                "atc_success_page": "[\"images\\/activity\\/ba847cdcf75077dddce6c718f72ec3d2.png\"]",//成功页面的背景集合
                "act_success_rules": "[\"346456\",\"645747654\"]",//成功页面的活动集合规则
                "title": "1", //活动的标题
                "start_time": "2018-04-25 00:00:00",//活动开始时间
                "end_time": "2018-04-30 23:59:00",//活动截止时间
                "desc": "1",//活动描述信息
                "atc_type": "0", //活动类型，0非支付：，1：支付类型
                "atc_type_value": "0", //当为支付类型的时候需要支付的值
                "gift_ids": "0"//此活动真正获取的id存在于此gift集合中，真正获取的id集合是它的子集
       }
   }
```

#### 参数说明
   |参数|类型|必须|说明|
   |:---|---|---|---|
   |act_id|int|是|活动id|
---

#### 活动发送短信验证码 方法
`POST /v4/activity/send-message`

####  json结构

```json
    {
       "errno": 0,
       "errmsg":"请求成功",
       "data": true  //活动短信验证码发送状态
   }
```

#### 参数说明
   |参数|类型|必须|说明|
   |:---|---|---|---|
   |phone|string|是|手机号码|
---

#### phone号码验证码是否正确 方法
`POST /v4/activity/check-sm-code`

####  json结构

```json
    {
       "errno": 0,
       "errmsg":"请求成功",
       "data": true  //手机号码验证码正确，且在有效期内
   }
```

#### 参数说明
   |参数|类型|必须|说明|
   |:---|---|---|---|
   |phone|string|是|手机号码|
   |sm_code|string|是|验证码|
---

#### 用户参加活动 方法
`POST /v4/activity/act-join`

####  json结构

```json
      {
          "errno": 0,
          "errmsg":"请求成功",
          "data": {
              "status": true, //活动参与是否成功的状态
              "info":"返回信息值" //活动参与后返回的活动需要的正确或错误的信息
           }
      }
```

#### 参数说明
   |参数|类型|必须|说明|
   |:---|---|---|---|
   |act_id|int|是|活动id|
   |phone|string|是|手机号码|
---


#### 获取用户参加活动最近一次的gift集合 方法
`POST /v4/activity/get-gift-pass-act-id`

####  json结构

```json
    {
       "errno": 0,
       "errmsg":"请求成功",
       "data": {
                "gift": [
                     [],  //每一gift的信息
                     []
                ]
       }
   }
```

#### 参数说明
   |参数|类型|必须|说明|
   |:---|---|---|---|
   |act_id|int|是|活动id|
   |phone|string|是|手机号码|
---






