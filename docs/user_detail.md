<!-- user_detail.md -->

# 用户信息

?> 查询当前登录人基本信息

|    接口名     | 请求方式 | 使用频率 |
| :-----------: | :------: | :------: |
| `user/detail` |   get    |  不常用  |

## 请求参数

| 参数 | 类型 | 必填 | 描述 |
| :--: | :--: | :--: | :--: |
|  无  |      |      |      |

## 返回参数

|   参数    |  类型  | 必填 |   描述    |
| :-------: | :----: | :--: | :-------: |
|   `id`    | string | true |  用户 id  |
|  `name`   | string | true |  用户名   |
|  `phone`  |  num   | true |  手机号   |
| `orgName` | double | true | 机构名称  |
| `orgLoge` | string | true | 机构 logo |

## 返回格式

```js
data:{
  id: "111",
  name: "小王",
  phone: "15099999999",
  orgName: "常州人社局",
  orgLoge: "https://CCDSAfs/sdafa/sdfa.jpg",
}

```
