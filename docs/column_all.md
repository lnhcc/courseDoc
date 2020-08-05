<!-- column_all.md -->

# 工种列表

?> 获取全部工种（二级）。

|    接口名    | 请求方式 | 使用频率 |
| :----------: | :------: | :------: |
| `column/all` |   get    |   常用   |

## 请求参数

| 参数 | 类型 | 必填 | 描述 |
| :--: | :--: | :--: | :--: |
|  无  |      |      |      |

## 返回参数

|        参数         | 类型 | 必填 |   描述   |
| :-----------------: | :--: | :--: | :------: |
| `data <columnList>` | list | true | 一级工种 |

### columnList 详细

|          参数          |  类型  | 必填  |     描述     |
| :--------------------: | :----: | :---: | :----------: |
|       `columnId`       | string | true  | 一级工种 id  |
|      `columnName`      | string | true  | 一级工种名称 |
|      `columnDesc`      | string | false | 一级工种描述 |
| `children <childList>` |  list  | true  | 二级工种列表 |

### childList 详细

|     参数     |  类型  | 必填  |     描述     |
| :----------: | :----: | :---: | :----------: |
|  `columnId`  | string | true  | 二级工种 id  |
| `columnName` | string | true  | 二级工种名称 |
| `columnDesc` | string | false | 二级工种描述 |

## 返回格式

```js
data: [
  {
    columnId: "1",
    columnName: "工种1",
    columnDesc: "啊啊啊1",
    children: [
      {
        columnId: "11",
        columnName: "工种11",
        columnDesc: "啊啊啊11",
      },
    ],
  },
  {
    columnId: "2",
    columnName: "工种2",
    columnDesc: "啊啊啊2",
    children: [
      {
        columnId: "21",
        columnName: "工种21",
        columnDesc: "啊啊啊21",
      },
    ],
  },
];
```
