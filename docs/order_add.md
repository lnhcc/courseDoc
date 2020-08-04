<!-- order_add.md -->

# 下单

?> 提交订单

|   接口名    | 请求方式 | 使用频率 |
| :---------: | :------: | :------: |
| `order/add` |   post   |   常用   |

## 请求参数

|   参数    |  类型  | 必填 |  描述   |
| :-------: | :----: | :--: | :-----: |
|   `id`    | string | true | 课程 id |
| `priceId` | string | true | 套餐 id |

## 返回参数

| 参数 | 类型 | 必填 | 描述 |
| :--: | :--: | :--: | :--: |
|  无  |      |      |      |

## 返回格式

```js
data: [
  {
    courseName: "课程名称11",
    courseType: 0,
    coursePrice: 10.0,
    courseDuration: "20",
    courseSection: "10",
  },
  {
    courseName: "课程名称12",
    courseType: 0,
    coursePrice: 10.0,
    courseDuration: "20",
    courseSection: "10",
  },
];
```
