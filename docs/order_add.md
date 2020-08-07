<!-- order_add.md -->

# 下单

?> 提交订单

|       接口名        | 请求方式 | 使用频率 |
| :-----------------: | :------: | :------: |
| `/public/order/add` |   post   |   常用   |

## 请求参数

|      参数      |  类型  | 必填 |        描述        |
| :------------: | :----: | :--: | :----------------: |
| `courseNumber` | string | true | 课程 course_number |
|   `priceId`    | string | true |      套餐 id       |
|    `amount`    | string | true |        数量        |

## 返回参数

| 参数 | 类型 | 必填 | 描述 |
| :--: | :--: | :--: | :--: |
|  无  |      |      |      |

## 返回格式

```json
{
  "message": "保存成功！",
  "code": "0"
}
```
