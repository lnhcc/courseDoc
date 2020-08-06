<!-- course_detail.md -->

# 课程

?> 根据课程 id 查询下详细信息。

|     接口名      | 请求方式 | 使用频率 |
| :-------------: | :------: | :------: |
| `course/detail` |   get    |   常用   |

## 请求参数

| 参数 |  类型  | 必填 |  描述   |
| :--: | :----: | :--: | :-----: |
| `id` | string | true | 课程 id |

## 返回参数

|             参数              |  类型  | 必填 |           描述            |
| :---------------------------: | :----: | :--: | :-----------------------: |
|          `courseId`           | string | true |          课程 id          |
|         `courseName`          | string | true |         课程名称          |
|         `courseType`          |  num   | true | 课程标签（0 普通 1 精品） |
|         `coursePrice`         | double | true |         课程售价          |
|         `courseDesc`          | string | true |        课程短描述         |
|       `courseDuration`        | string | true |      课程时长 (min)       |
|        `courseSection`        | string | true |        课程总章节         |
|         `courseIntro`         | string | true |     课程简介 (富文本)     |
|    `courseSet <priceList>`    |  list  | true |           套餐            |
| `courseTeacher <teacherList>` |  list  | true |           讲师            |

### priceList 详细

|     参数     |  类型  | 必填  |   描述    |
| :----------: | :----: | :---: | :-------: |
|  `priceId`   | string | true  |  套餐 id  |
| `priceName`  | string | true  | 套餐 名称 |
| `priceDesc`  | string | false | 套餐 描述 |
| `priceMoney` |  list  | true  | 套餐价格  |

### teacherList 详细

|     参数      |  类型  | 必填  |   描述    |
| :-----------: | :----: | :---: | :-------: |
|  `teacherId`  | string | true  |  讲师 id  |
| `teacherName` | string | true  | 讲师 名称 |
| `teacherDesc` | string | false | 讲师 描述 |

## 返回格式

```js
data:
  {
    courseId: "112123",
    courseName: '课程名称11',
    courseType: 0,
    coursePrice: 20.0,
    courseDesc: "描啊啊啊",
    courseIntro: "<div>我是介绍</div>",
    courseDuration:'30',
    courseSection:'5'
    priceList: [{
      priceId:'',
      priceName:'',
      priceDesc:'',
      priceMoney:''
    }],
    teacherList: [{
      teacherId:'',
      teacherName:'',
      teacherDesc:'',
    }],
  },

```
