
# 小程序应用活动API

##  H5页面使用

### 根据活动id获取活动页面信息

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

### 活动发送短信验证码 方法
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

### phone号码验证码是否正确 方法
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

### 用户参加活动 方法
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

### 获取用户关于某一场活动的gift集合 方法
`POST /v4/user/gift-pass-act-id`

```
type =0     //表示返回活动id最近一次的gift集合
type = 1 //返回用户关于活动id的gift所有集合
```

####  json结构

```json
{
    "errno": 0,
    "errmsg": "请求成功",
    "data": [
        {
            "id": "5",
            "uid": "42700001",
            "gift_id": "5",
            "gift_valid_value": "5",
            "act_id": "3",
            "entrance_id": "2",
            "get_date": "2018-05-07",
            "get_time": "2018-05-07 10:05:37",
            "signboard": "5819f3ad1c0ce",
            "status": "1",
            "partner": "必胜客",
            "names": "必胜客必胜客",
            "desc": "必胜客必胜客必胜客必胜客",
            "background_url": "720884288973fd14a50b6a1f10ac0f4d2ce39a35.jpg",
            "thumbnail": "0",
            "to_use_value": "5",
            "to_use_value_max": "2",
            "to_use_value_min": "-1",
            "to_use_type": "0",
            "back_type": "0",
            "use_condition": "{\"18\":{\"id\":\"18\",\"start_time\":\"2018-02-08 06:03:02\",\"end_time\":\"2018-09-08 06:03:02\"},\"19\":{\"id\":\"19\",\"start_day\":\"-1\",\"end_num\":\"66\"},\"20\":{\"id\":\"20\"}}",
            "get_rules": "{\"23\":{\"id\":\"23\",\"prob\":\"12\"}}",
            "sort": "12",
            "create_time": "2018-04-26 03:50:31",
            "distribution_status": "1",
            "gift_num": "2"
        },
        {
            "id": "6",
            "uid": "42700001",
            "gift_id": "6",
            "gift_valid_value": "5",
            "act_id": "3",
            "entrance_id": "2",
            "get_date": "2018-05-07",
            "get_time": "2018-05-07 11:01:05",
            "signboard": "5819f3ad1c0ce",
            "status": "1",
            "partner": "测试",
            "names": "测试",
            "desc": "测试",
            "background_url": "a40a9fdec8434fd53b9c5ba11f6b39fb9655ff72.jpg",
            "thumbnail": "0",
            "to_use_value": "2",
            "to_use_value_max": "1",
            "to_use_value_min": "-1",
            "to_use_type": "0",
            "back_type": "0",
            "use_condition": "0",
            "get_rules": "0",
            "sort": "12",
            "create_time": "2018-04-26 03:56:15",
            "distribution_status": "1",
            "gift_num": "1"
        }
    ]
}
```

#### 参数说明
   |参数|类型|必须|说明|
   |:---|---|---|---|
   |act_id|int|是|活动id|
   |phone|string|是|手机号码|
   |type|int|是|获取活动gift类型|
---

### 展示用户gift的方法
`POST /v4/user/get-gift`

#### gift_type 用于用户的gift返回数据格式定义
```
gift_type = 0 //用户红包类型数据返回
gift_type = 1 //用户卡，券类型数据返回
```


####  gift_type=0 的json结构

```json
{
    "errno": 0,
    "errmsg": "请求成功",
    "data":"1314"  //用户的红包金额
}
```

####  gift_type=1 的json结构

```json
{
    "errno": 0,
    "errmsg": "请求成功",
    "data": [
        {
            "id": "5",
            "uid": "42700001",
            "gift_id": "5",
            "gift_valid_value": "5",
            "act_id": "3",
            "entrance_id": "2",
            "get_date": "2018-05-07",
            "get_time": "2018-05-07 10:05:37",
            "signboard": "5819f3ad1c0ce",
            "status": "1",
            "partner": "必胜客",
            "names": "必胜客必胜客",
            "desc": "必胜客必胜客必胜客必胜客",
            "background_url": "720884288973fd14a50b6a1f10ac0f4d2ce39a35.jpg",
            "thumbnail": "0",
            "to_use_value": "5",
            "to_use_value_max": "2",
            "to_use_value_min": "-1",
            "to_use_type": "0",
            "back_type": "0",
            "use_condition": "{\"18\":{\"id\":\"18\",\"start_time\":\"2018-02-08 06:03:02\",\"end_time\":\"2018-09-08 06:03:02\"},\"19\":{\"id\":\"19\",\"start_day\":\"-1\",\"end_num\":\"66\"},\"20\":{\"id\":\"20\"}}",
            "get_rules": "{\"23\":{\"id\":\"23\",\"prob\":\"12\"}}",
            "sort": "12",
            "create_time": "2018-04-26 03:50:31",
            "distribution_status": "1",
            "gift_num": "2"
        }
    ]
}
```


#### 参数说明
   |参数|类型|必须|说明|
   |:---|---|---|---|
   |uid|int|是|用户uid|
   |gift_type|int|是|gift类型的集合|
---

### 扫码开门
`POST /v4/bus/open-door`

####  json结构

```json
   {
     "errno": 0,
     "errmsg": "请求成功",
     "data": {
       "uid": "42700001",
       "club_id": "4",
       "order_no": "051517101542700001",
       "order_amount": "3.00", //本次订单需要支付的费用
       "pre_amount": 0,      //用户优惠的费用
       "pay_amount": 3,      //用户支付的费用
       "order_long": 3780,   //订单能够维持用户锻炼的时常，正常为3600，若使用了gift，则可边长
       "pay_no": "051517101542700001"
     }
   }
```

#### 参数说明
   |参数|类型|必须|说明|
   |:---|---|---|---|
   |club_id|int|是|门店di|
   |uid|int|是|用户uid|
---