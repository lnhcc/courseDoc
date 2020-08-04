<!-- course_section.md -->

# 课程的章节

?> 根据课程 id 查询章节。

|      接口名      | 请求方式 | 使用频率 |
| :--------------: | :------: | :------: |
| `course/section` |   get    |   常用   |

## 请求参数

| 参数 |  类型  | 必填 |  描述   |
| :--: | :----: | :--: | :-----: |
| `id` | string | true | 课程 id |

## 返回参数

|         参数          |  类型  | 必填 |    描述     |
| :-------------------: | :----: | :--: | :---------: |
|         `id`          | string | true |    章 id    |
|        `name`         | string | true |   章名称    |
|        `time`         | string | true | 时长（min） |
| `children <nodeList>` |  list  | true |     节      |

### nodeList 详细

|  参数  |  类型  | 必填 |    描述     |
| :----: | :----: | :--: | :---------: |
|  `id`  | string | true |    节 id    |
| `name` | string | true |   节名称    |
| `time` | string | true | 时长（min） |

## 返回格式

```js
data: [
  {
    id: "1",
    name: "章1",
    time: "10",
    children: [
      {
        id: "2",
        name: "节1",
        time: "10",
      },
    ],
  },
  {
    id: "3",
    name: "章2",
    time: "20",
    children: [
      {
        id: "4",
        name: "节2",
        time: "10",
      },
      {
        id: "5",
        name: "节3",
        time: "10",
      },
    ],
  },
];
```
