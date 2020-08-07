<!-- course_home.md -->

# 课程列表

?> 根据栏目 id 和其他搜索条件查询课程。

|        接口名         | 请求方式 | 使用频率 |
| :-------------------: | :------: | :------: |
| `/public/course/page` |   post   |   常用   |

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
|  `courseNumber`  | string | true |    课程 course_number     |
|      `name`      | string | true |         课程名称          |
| `isFineDesigned` | double | true | 课程标签（0 普通 1 精品） |
|    `perPrice`    | double | true |         课程售价          |
|  `videoPeriod`   |  num   | true |      课程时长 (min)       |
| `sectionAmount`  |  num   | true |        课程总章节         |

## 返回格式

```js
data: [
  {
    courseNumber: "",
    name: "课程名称12",
    isFineDesigned: 0,
    perPrice: 10.0,
    videoPeriod: "20",
    sectionAmount: "10",
  },
  {
    courseNumber: "",
    name: "课程名称12",
    isFineDesigned: 0,
    perPrice: 10.0,
    videoPeriod: "20",
    sectionAmount: "10",
  },
];
```
