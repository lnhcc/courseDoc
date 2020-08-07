<!-- order_list.md -->

# 订单查询

?> 客户查询自己的订单列表

|        接口名        | 请求方式 | 使用频率 |
| :------------------: | :------: | :------: |
| `/public/order/page` |   post   |   常用   |

## 请求参数 (需要分页)

|    参数    |  类型  | 必填  |  描述  |
| :--------: | :----: | :---: | :----: |
| courseName | string | false | 课程名 |

## 返回参数

|    参数     | 类型 | 必填 |   描述   |
| :---------: | :--: | :--: | :------: |
| `orderList` | list | true | 订单列表 |

### orderList 详细

|     参数      |  类型  | 必填 |                      描述                       |
| :-----------: | :----: | :--: | :---------------------------------------------: |
|     `id`      | string | true |                     订单 id                     |
| `orderNumber` | string | true |                     订单号                      |
|    `total`    | double | true |                     总金额                      |
|  `createdBy`  | string | true |                     下单人                      |
|   `status`    |  num   | true | 订单状态（0 待支付 1 已支付 2 已取消 3 已退款） |
|  `children`   |  list  | true |                    订单明细                     |

### courseList 详细

|         参数          |  类型  | 必填 |                      描述                       |
| :-------------------: | :----: | :--: | :---------------------------------------------: |
|    `courseNumber`     | string | true |               课程 course_number                |
|     `courseName`      | string | true |                    课程名称                     |
|    `merchantName`     | string | true |                     供课商                      |
|     `packageName`     | string | true |                     套餐名                      |
| `actualPaymentAmount` | double | true |                      实付                       |
|       `status`        |  num   | true | 订单状态（0 待支付 1 已支付 2 已取消 3 已退款） |
|    `isAuthorized`     |  num   | true |     授权状态(0 待授权 1 已授权 2 取消授权)      |

## 返回格式

```js
data: [
  {
    id: "327237247",
    orderNumber: "112322342342",
    total: 10.0,
    createdBy: "小王",
    status: 0,
    children: [
      {
        courseNumber: "11",
        courseName: "插画艺术",
        merchantName: "商户1",
        packageName: "套餐AAA",
        actualPaymentAmount: 10.0,
        status: 0,
        isAuthorized: 1,
      },
    ],
  },
  {
    id: "3332443",
    orderNumber: "112322342342",
    total: 10.0,
    createdBy: "小王",
    status: 0,
    children: [
      {
        courseNumber: "11",
        courseName: "插画艺术",
        merchantName: "商户1",
        packageName: "套餐AAA",
        actualPaymentAmount: 10.0,
        status: 0,
        isAuthorized: 1,
      },
    ],
  },
];
```
