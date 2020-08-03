<!-- course_home.md -->

# 课程列表

?> 根据栏目 id 和其他搜索条件查询课程。

|    接口名     | 请求方式 | 使用频率 |
| :-----------: | :------: | :------: |
| `course/list` |   get    |   常用   |

## 请求参数

|     参数      |  类型  | 必填  |                       描述                       |
| :-----------: | :----: | :---: | :----------------------------------------------: |
|  `columnId`   | string | false |                     工种 id                      |
|    `sort`     | string | false |         排序(0 最新、1 最热、2 评论最多)         |
|    `time`     | string | false | 时间（0 今年、1 最近一个月、2 最近一周、3 今天） |
| `searchValue` | string | false |                课程名称或讲师名称                |

## 返回参数

|        参数         | 类型 | 必填 |   描述   |
| :-----------------: | :--: | :--: | :------: |
| `data <CourseList>` | list | true | 分类数组 |

## CourseList 详细

|        参数        |  类型  | 必填 |     描述     |
| :----------------: | :----: | :--: | :----------: |
|    `courseName`    | string | true |   课程名称   |
|    `courseDesc`    | string | true |   课程描述   |
|   `coursePrice`    | double | true |   课程售价   |
| `courseWatchCount` | number | true | 课程观看人数 |
| `courseSaleCount`  | number | true | 课程售卖次数 |

## 返回格式

```js
data: [
  {
    courseName: "课程名称11",
    coursePrice: 10.0,
    courseWatchCount: 20,
    courseSaleCount: 1,
  },
  {
    courseName: "课程名称12",
    coursePrice: 10.0,
    courseWatchCount: 20,
    courseSaleCount: 1,
  },
];
```
