<!-- column_all.md -->

# 获取二级栏目

?> 根据一级栏目 id,获取二级栏目。

|       接口名        | 请求方式 | 使用频率 |
| :-----------------: | :------: | :------: |
| `column/byColumnId` |   get    |   常用   |

## 请求参数

|   参数   |  类型  | 必填  |                       描述                        |
| :------: | :----: | :---: | :-----------------------------------------------: |
| columnId | string | false | 一级栏目 id (为空的时候 返回第一个栏目下的子栏目) |

## 返回参数

|        参数         | 类型 | 必填 |   描述   |
| :-----------------: | :--: | :--: | :------: |
| `data <columnList>` | list | true | 二级栏目 |

### columnList 详细

|     参数     |  类型  | 必填  |     描述     |
| :----------: | :----: | :---: | :----------: |
|  `columnId`  | string | true  | 二级栏目 id  |
| `columnName` | string | true  | 二级栏目名称 |
| `columnDesc` | string | false | 二级栏目描述 |

## 返回格式

```js
data: [
  {
    columnId: "11",
    columnName: "栏目11",
    columnDesc: "啊啊啊1",
  },
  {
    columnId: "12",
    columnName: "栏目12",
    columnDesc: "啊啊啊2",
  },
];
```
