<!-- order_list.md -->

# 订单查询

?> 客户查询自己的订单列表

|    接口名    | 请求方式 | 使用频率 |
| :----------: | :------: | :------: |
| `order/list` |   post   |   常用   |

## 请求参数 (需要分页)

|    参数     |  类型  | 必填  |  描述  |
| :---------: | :----: | :---: | :----: |
| searchVaule | string | false | 课程名 |

## 返回参数

|        参数        | 类型 | 必填 |   描述   |
| :----------------: | :--: | :--: | :------: |
| `data <orderList>` | list | true | 订单列表 |

### orderList 详细

|          参数           |  类型  | 必填 |                      描述                       |
| :---------------------: | :----: | :--: | :---------------------------------------------: |
|          `id`           | string | true |                     订单 id                     |
|          `num`          | string | true |                     订单号                      |
|         `money`         | double | true |                     总金额                      |
|       `userName`        | string | true |                     下单人                      |
|         `state`         |  num   | true | 订单状态（0 待支付 1 已支付 2 已取消 3 已退款） |
| `children <courseList>` |  list  | true |                    订单明细                     |

### courseList 详细

|     参数     |  类型  | 必填 |                      描述                       |
| :----------: | :----: | :--: | :---------------------------------------------: |
|     `id`     | string | true |                     课程 id                     |
|    `name`    | string | true |                    课程名称                     |
|  `merchant`  | string | true |                     供课商                      |
|  `setName`   | string | true |                     套餐名                      |
|   `money`    | double | true |                      实付                       |
|   `state`    |  num   | true | 订单状态（0 待支付 1 已支付 2 已取消 3 已退款） |
| `powerState` |  num   | true |     授权状态(0 待授权 1 已授权 2 取消授权)      |

## 返回格式

```js
data: [
  {
    id: "327237247",
    num: "112322342342",
    money: 10.0,
    userName: "小王",
    state: 0,
    children: [
      {
        id: "11",
        name: "插画艺术",
        merchant: "商户1",
        setName: "套餐AAA",
        money: 10.0,
        state: 0,
        powerState: 1,
      },
    ],
  },
  {
    id: "3332443",
    num: "52345325243",
    money: 10.0,
    userName: "小王",
    state: 0,
    children: [
      {
        id: "11",
        name: "插画艺术",
        merchant: "商户1",
        setName: "套餐AAA",
        money: 10.0,
        state: 0,
        powerState: 1,
      },
    ],
  },
];
```
