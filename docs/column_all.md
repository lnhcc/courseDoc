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

|          参数          |  类型  | 必填 |     描述     |
| :--------------------: | :----: | :--: | :----------: |
|        `value`         | string | true | 一级工种 key |
|        `label`         | string | true | 一级工种名称 |
| `children <childList>` |  list  | true | 二级工种列表 |

### childList 详细

|     参数      |  类型  | 必填 |     描述     |
| :-----------: | :----: | :--: | :----------: |
| `columnValue` | string | true | 二级工种 key |
| `columnLabel` | string | true | 二级工种名称 |

## 返回格式

```js
data: [
  {
    value: "1",
    label: "工种1",
    children: [
      {
        columnValue: "11",
        columnLabel: "工种11",
      },
    ],
  },
  {
    value: "2",
    label: "工种2",
    children: [
      {
        columnValue: "21",
        columnLabel: "工种21",
      },
    ],
  },
];
```

<!-- data:{
  '工种1':[{name:'工种11'},{name:'工种12'}],
  '工种2':[{name:'工种21'},{name:'工种22'}],
  '工种3':[{name:'工种31'},{name:'工种32'}],
  '工种4':[{name:'工种41'},{name:'工种42'}],
} -->
