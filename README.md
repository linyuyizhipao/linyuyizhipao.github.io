
# 小程序应用活动API

##  H5页面使用

### 根据活动id获取活动页面信息

 ```
 act_id = 3          // 用于确认参与哪一个活动的ID
 ```
 
#### 汇总参数 方法

`POST http://localhost:8000/v4/activity/act-get-info`

####  json结构

```json
    {
       "result": true,
       "statusCode": 0,
       "userData": {
           "user_total": "147",  //总会员数
           "everyshop": [
               {
                   "user_num": "111",  //门店总会员数
                   "shop_id": "60021", //门店id
                   "shop_name": "开发门店1"  //门店名称
               }
           ]
       }
   }
```

#### 参数说明
   |参数|类型|必须|说明|
   |:---|---|---|---|
   |type_id|string|是|模块属性|
   |start_time|date|否|开始时间|
   |end_time|date|否|结束时间|
   |source|string|是|二级渠道|
---

#### 门店会员分布 方法
`GET c=BdpUser&a=shopusercount&type_id=is_column`

####  json结构

```json
      {
          "errno": "0",
          "errmsg": "请求成功",
          "data": {
              "level_all": [
                  {
                      "name": "木牌",//会员等级名称
                      "id": "1"      //会员等级id
                  },
                  {
                      "name": "金牌",
                      "id": "33"
                  }
              ],
              "everyshop": [
                      {
                          "shop_name": "开发门店1",//门店名称
                          "shop_id": "60021",     //门店id
                          "shop_all": [
                              {
                                  "user_num ": "81",//会员个数
                                  "user_level ": "1",//会员等级id
                                  "name ": "木牌"    //等级名称
                              },
                              {
                                  "user_num ": "4",
                                  "user_level ": "33",
                                  "name ": "金牌"
                              }
                          ]
                      }
              ]
          }
      }
```

#### 参数说明
   |参数|类型|必须|说明|
   |:---|---|---|---|
   |type_id|string|是|模块属性|
   |start_time|date|否|开始时间|
   |end_time|date|否|结束时间|
   |source|string|是|二级渠道|
   |user_level|int|否|筛选会员等级|
---

#### 门店会员汇总列表 方法
`GET c=BdpUser&a=shopusercount&type_id=list`

####  json结构

```json
      {
           "errno": "0",
           "errmsg": "请求成功",
           "data": {
               "shop_all": [//所有有会员的门店
                   {
                       "user_num": "111", //门店会员总数
                       "shop_id": "60021",//门店id
                       "name": "开发门店1"//门店名称
                   },
                   {
                       "user_num": "1",
                       "shop_id": "60023",
                       "name": "--"
                   }
               ],
               "total": "3",//总条数
               "result": [
                   {
                       "0": {
                           "shop_id": "60021",//门店id
                           "total_num": "1"   //门店人数
                       },
                       "1": {
                           "shop_id": "60023",//门店人数
                           "total_num": "0"   //门店id
                       },
                       "one_day": "2017-11-29" //注册时间
                   }
               ]
           }
      }
```

#### 参数说明
   |参数|类型|必须|说明|
   |:---|---|---|---|
   |type_id|string|是|模块属性|
   |start_time|date|否|开始时间|
   |end_time|date|否|结束时间|
   |source|string|是|二级渠道|
   |page|int|否|页数|
   |limit|int|否|每页条数|
---

## 客群分析

### type_id类型定义
 ```
 type_id = is_pie_1    // 新老会员比
 type_id = is_pie_2    // 活跃会员与沉睡会员比
 type_id = is_pie_3    // 忠诚会员与流失会员比
 ```
 
#### 新老会员比 方法
`GET c=BdpUser&a=customer&type_id=is_pie_1`

####  json结构

```json
    {
        "errno": "0",
        "errmsg": "请求成功",
        "data": {
            "new": {
                "user": "112",    //新会员
                "ratio": "76.19%" //新会员占比
            },
            "old": {
                "user": "35",     //老会员
                "ratio": "23.81%" //老会员占比
            },
            "all_user": "147"     //总会员
        }
    }
```

#### 参数说明
   |参数|类型|必须|说明|
   |:---|---|---|---|
   |type_id|string|是|模块属性|
   |start_time|date|否|开始时间|
   |end_time|date|否|结束时间|
   |source|string|是|二级渠道|
---

#### 活跃会员与沉睡会员比 方法
`GET c=BdpUser&a=customer&type_id=is_pie_2`

####  json结构

```json
      {
          "errno": "0",
          "errmsg": "请求成功",
          "data": {
              "all_user": "147",           //总会员
              "active": {
                  "active_user": "15",     //活跃会员
                  "active_ratio": "10.20%" //活跃会员占比
              },
              "sleep": {
                  "sleep_user": "112",     //沉睡会员
                  "sleep_ratio": "89.8%"   //沉睡会员占比
              }
          }
      }
```

#### 参数说明
   |参数|类型|必须|说明|
   |:---|---|---|---|
   |type_id|string|是|模块属性|
   |start_time|date|否|开始时间|
   |end_time|date|否|结束时间|
   |source|string|是|二级渠道|
   |min|int|否|消费最小次数值|
   |max|int|否|消费最大次数值|
---

#### 忠诚会员与流失会员比 方法
`GET c=BdpUser&a=customer&type_id=is_pie_3`

####  json结构

```json
      {
          "errno": "0",
          "errmsg": "请求成功",
          "data": {
              "all_user": "147",     //总会员数
              "loyal": {
                  "loyal_user": "72",//忠诚会员
                  "loyal_ratio": "48.98%"//忠诚会员比
              },
              "loss": {
                  "loss_user": "75",    //流失会员
                  "loss_ratio": "51.02%"//流失会员比
              }
          }
      }
```

#### 参数说明
   |参数|类型|必须|说明|
   |:---|---|---|---|
   |type_id|string|是|模块属性|
   |start_time|date|否|开始时间|
   |end_time|date|否|结束时间|
   |source|string|是|二级渠道|
---

## 客单价分析

### type_id类型定义
 ```
 type_id = test         // 总的平均客单价
 type_id = is_pie_1    // 新会员客单价阶段比
 type_id = is_pie_2    // 老会员客单价阶段比
 ```
 
#### 总的平均客单价 方法
`GET c=BdpUser&a=shopprice&type_id=test`

####  json结构

```json
    {
        "errno": "0",
        "errmsg": "请求成功",
        "data": {
            "unit_price": "31031.06", //平均客单价
            "new_price": "13232.36",  //新会员平均客单价
            "old_price": "68925.07"   //老会员平均客单价
        }
    }
```

#### 参数说明
   |参数|类型|必须|说明|
   |:---|---|---|---|
   |type_id|string|是|模块属性|
   |start_time|date|否|开始时间|
   |end_time|date|否|结束时间|
   |source|string|是|二级渠道|
---

#### 新会员客单价阶段比 方法
`GET c=BdpUser&a=shopprice&type_id=is_pie_1`

####  json结构

```json
      {
          "errno": "0",
          "errmsg": "请求成功",
          "data": {
              "total_amount": "873834.72",//总金额
              "total_num": "153",         //总人数
              "data": {
                  "0": {
                      "amount": "7460.67",//价格区间总金额
                      "num": "42",        //购买0-50之间的会员数
                      "ratio": "27.45%"   //会员人数占比
                  },
                  "51": {
                      "amount": "23790.15",//价格区间总金额
                      "num": "24",        //购买51-100之间的会员数
                      "ratio": "15.69%"   //会员人数占比
                  },
                  "101": {
                      "amount": "8639.66",//价格区间总金额
                      "num": "12",        //购买101-150之间的会员数
                      "ratio": "7.84%"    //会员人数占比
                  },
                  "151": {
                      "amount": "5850.22",//价格区间总金额
                      "num": "13",        //购买151-200之间的会员数
                      "ratio": "8.5%"     //会员人数占比
                  },
                  "201": {
                      "amount": "7286.90",//价格区间总金额
                      "num": "9",         //购买201-250之间的会员数
                      "ratio": "5.88%"    //会员人数占比
                  },
                  "251": {
                      "amount": "6018.80",//价格区间总金额
                      "num": "10",        //购买251-300之间的会员数
                      "ratio": "6.54%"    //会员人数占比
                  },
                  "301": {
                      "amount": "3978.64",//价格区间总金额
                      "num": "8",         //购买301-350之间的会员数
                      "ratio": "5.23%"    //会员人数占比
                  },
                  "350": {
                      "amount": "810809.68",//价格区间总金额
                      "num": "35",          //购买350元以上的会员数
                      "ratio": "22.88%"     //会员人数占比
                  }
              }
          }
      }
```

#### 参数说明
   |参数|类型|必须|说明|
   |:---|---|---|---|
   |type_id|string|是|模块属性|
   |start_time|date|否|开始时间|
   |end_time|date|否|结束时间|
   |source|string|是|二级渠道|
---

#### 老会员客单价阶段比 方法
`GET c=BdpUser&a=shopprice&type_id=is_pie_2`

####  json结构

```json
      {
          "errno": "0",
          "errmsg": "请求成功",
          "data": {
              "total_amount": "3794",//总金额
              "total_num": "28",     //总人数
              "data": {
                  "0": {
                      "amount": "0",//价格区间总金额
                      "num": "0",
                      "ratio": "0%"//会员人数占比
                  },
                  "51": {
                      "amount": "0",//价格区间总金额
                      "num": "0",
                      "ratio": "0%"//会员人数占比
                  },
                  "101": {
                      "amount": "3794.00",//价格区间总金额
                      "num": "28",
                      "ratio": "100%"//会员人数占比
                  },
                  "151": {
                      "amount": "0",//价格区间总金额
                      "num": "0",
                      "ratio": "0%"//会员人数占比
                  },
                  "201": {
                      "amount": "0",//价格区间总金额
                      "num": "0",
                      "ratio": "0%"//会员人数占比
                  },
                  "251": {
                      "amount": "0",//价格区间总金额
                      "num": "0",
                      "ratio": "0%"//会员人数占比
                  },
                  "301": {
                      "amount": "0",//价格区间总金额
                      "num": "0",
                      "ratio": "0%"//会员人数占比
                  },
                  "350": {
                      "amount": "0",//价格区间总金额
                      "num": "0",
                      "ratio": "0%"//会员人数占比
                  }
              }
          }
      }
```

#### 参数说明
   |参数|类型|必须|说明|
   |:---|---|---|---|
   |type_id|string|是|模块属性|
   |start_time|date|否|开始时间|
   |end_time|date|否|结束时间|
   |source|string|是|二级渠道|
---


