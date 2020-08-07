<!-- course_section.md -->

# 课程的章节

?> 根据课程 id 查询章节。

|          接口名          | 请求方式 | 使用频率 |
| :----------------------: | :------: | :------: |
| `/public/course/section` |   post   |   常用   |

## 请求参数

|      参数      |  类型  | 必填 |        描述        |
| :------------: | :----: | :--: | :----------------: |
| `courseNumber` | string | true | 课程 course_number |

## 返回参数

|    参数     |  类型  | 必填 |  描述  |
| :---------: | :----: | :--: | :----: |
| `chapterId` | string | true | 章 id  |
|   `name`    | string | true | 章名称 |
| `orderDesc` | string | true | 章序号 |
| `children`  |  list  | true |   节   |

### children 详细

|    参数     |  类型  | 必填 |    描述     |
| :---------: | :----: | :--: | :---------: |
| `sectionId` | string | true |    节 id    |
|   `name`    | string | true |   节名称    |
| `orderDesc` | string | true |   节序号    |
|  `period`   | string | true | 时长（min） |

## 返回格式

```js
data: [
  {
    chapterId: "1",
    name: "章1",
   orderDesc:"第1章",
    children: [
      {
        sectionId: "2",
        name: "节1",
        orderDesc:"第3节"，
       period: "10",
      },
    ],
  },
  {
    chapterId: "1",
    name: "章2",
   orderDesc:"第2章",
    children: [
      {
        sectionId: "2",
        name: "节1",
        orderDesc:"第3节"，
       period: "10",
      },
    ]
  },
];
```
