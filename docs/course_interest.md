<!-- course_interest.md -->

# 感兴趣的课程

?> 根据课程 id 查询相似的课程（五个）。

|          接口名           | 请求方式 | 使用频率 |
| :-----------------------: | :------: | :------: |
| `/public/course/interest` |   post   |   常用   |

## 请求参数

|      参数      |  类型  | 必填  |        描述        |
| :------------: | :----: | :---: | :----------------: |
| `courseNumber` | string | false | 课程 course_number |

## 返回参数

|     参数     | 类型 | 必填 |   描述   |
| :----------: | :--: | :--: | :------: |
| `courseList` | list | true | 课程列表 |

### courseList 详细

|       参数       |  类型  | 必填 |           描述            |
| :--------------: | :----: | :--: | :-----------------------: |
|  `courseNumber`  | string | true |          课程 id          |
|      `name`      | string | true |         课程名称          |
| `isFineDesigned` |  num   | true | 课程标签（0 普通 1 精品） |
|  `introduction`  | string | true |        课程短描述         |
|  `videoPeriod`   | string | true |      课程时长 (min)       |
| `sectionAmount:` | string | true |        课程总章节         |
|   `objective`    | string | true |     课程简介 (富文本)     |

## 返回格式

```js
data: [
  {
    courseNumber: "112123",
    name: "课程名称11",
    isFineDesigned: 0,
    introduction: 20.0,
    videoPeriod: "1515",
    sectionAmount: "226",
    objective: "课程主要/。。。。",
  },
  {
    courseNumber: "112123",
    name: "课程名称11",
    isFineDesigned: 0,
    introduction: 20.0,
    videoPeriod: "1515",
    sectionAmount: "226",
    objective: "课程主要/。。。。",
  },
];
```
