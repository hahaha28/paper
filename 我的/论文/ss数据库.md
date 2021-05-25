# ss数据库

用户表

```json
{
    "_id" : "用户的唯一id，由MongoDB自动生成的ObjectID格式",
    "tel" : "用户手机号"
}
```

菜品表

```json
{
    "_id" : "菜品的唯一id，由MongoDB自动生成的ObjectID格式",
    "description" : "菜品描述",
    "groupID" : "菜品所属的分组的id",
    "name" : "菜品名",
    "positiveRate" : "好评率",
    "price" : "价格",
    "sales" : "销量",
    "picPath" : "图片在服务器上的相对路径",
    "pic" : "图片的url相对路径",
    "ingredient" :[
        {
            "inName" : "材料名",
            "inNeed" : "数量",
            "inUnit" : "单位"
        }
    ]
}
```

菜品分组表

```json
{
    "_id" : "菜品的唯一id，由MongoDB自动生成的ObjectID格式",
    "name" : "菜品分组名",
    "userID" : "创建该分组的用户id",
    "dishIDs" : [
        "分组内的菜品id"
    ]
}
```

订单表

```json
{
    "_id" : "订单的唯一id，由MongoDB自动生成的ObjectID格式",
    "customerID" : "下单的顾客的id",
    "restaurantID" : "餐厅的id",
    "dishes" : [
        {
            "dishID" : "菜品的id",
            "num" : "数量"
        }
    ],
    "cost" : "花费",
	"takeFoodCode" : "取餐码",
    "createTime" : "订单创建时间",
    "finishTime" : "订单完成时间",
    "status" : "订单状态（已完成、进行中）"
}
```

反馈表

```json
{
    "_id" : "反馈的唯一id，由MongoDB自动生成的ObjectID格式",
    "customerID" : "反馈的顾客的id",
    "restaurantID" : "餐厅的id",
    "suggestion" : "建议",
    "timestamp" : "时间戳"
}
```

