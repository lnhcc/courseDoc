<!-- course_interest.md -->

# 感兴趣的课程

?> 根据课程 id 查询相似的课程（五个）。

|      接口名       | 请求方式 | 使用频率 |
| :---------------: | :------: | :------: |
| `course/interest` |   get    |   常用   |

## 请求参数

| 参数 |  类型  | 必填  |  描述   |
| :--: | :----: | :---: | :-----: |
| `id` | string | false | 课程 id |

## 返回参数

|        参数         | 类型 | 必填 |   描述   |
| :-----------------: | :--: | :--: | :------: |
| `data <CourseList>` | list | true | 课程列表 |

### CourseList 详细

|       参数       |  类型  | 必填 |           描述            |
| :--------------: | :----: | :--: | :-----------------------: |
|    `courseId`    | string | true |          课程 id          |
|   `courseName`   | string | true |         课程名称          |
|   `courseType`   | double | true | 课程标签（0 普通 1 精品） |
|  `coursePrice`   | double | true |         课程售价          |
| `courseDuration` |  num   | true |      课程时长 (min)       |
| `courseSection`  |  num   | true |        课程总章节         |

## 返回格式

```js
data: [
  {
    courseId: "",
    courseName: "课程名称12",
    courseType: 0,
    coursePrice: 10.0,
    courseDuration: "20",
    courseSection: "10",
  },
  {
    courseId: "",
    courseName: "课程名称12",
    courseType: 0,
    coursePrice: 10.0,
    courseDuration: "20",
    courseSection: "10",
  },
];
```
