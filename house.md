
# 租房系统api开发文档

##  house对象

### 根据房东uid展示房源下的所有房子信息

`GET http://www.hushuang.site:8080/backend/landlord/show-house-resouce`

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
   ||uid|string|是|房东id|


### 根据房东uid展示房源列表

`GET http://www.hushuang.site:8080/backend/landlord/house-resouce-list`

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
   |house_id|string|是|房源id|

