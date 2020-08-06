<!-- course_home.md -->

# 课程列表

?> 根据栏目 id 和其他搜索条件查询课程。

|    接口名     | 请求方式 | 使用频率 |
| :-----------: | :------: | :------: |
| `course/list` |   get    |   常用   |

## 请求参数 (需要分页)

|      参数       |  类型  | 必填  |                       描述                       |
| :-------------: | :----: | :---: | :----------------------------------------------: |
|   `columnId`    | string | false |         栏目 id（id 为空 返回所有课程）          |
| `sort` (先不做) | string | false |         排序(0 最新、1 最热、2 评论最多)         |
| `time` (先不做) | string | false | 时间（0 今年、1 最近一个月、2 最近一周、3 今天） |
|  `searchValue`  | string | false |                课程名称或讲师名称                |

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
