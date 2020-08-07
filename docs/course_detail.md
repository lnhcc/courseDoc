<!-- course_detail.md -->

# 课程

?> 根据课程 id 查询下详细信息。

|         接口名          | 请求方式 | 使用频率 |
| :---------------------: | :------: | :------: |
| `/public/course/detail` |   post   |   常用   |

## 请求参数

|      参数      |  类型  | 必填 |        描述        |
| :------------: | :----: | :--: | :----------------: |
| `courseNumber` | string | true | 课程 course_number |

## 返回参数

|       参数       |     类型      | 必填 |           描述            |
| :--------------: | :-----------: | :--: | :-----------------------: |
|  `courseNumber`  |    string     | true |          课程 id          |
|      `name`      |    string     | true |         课程名称          |
| `isFineDesigned` |      num      | true | 课程标签（0 普通 1 精品） |
|  `introduction`  |    string     | true |        课程短描述         |
|  `videoPeriod`   |    string     | true |      课程时长 (min)       |
| `sectionAmount`  |    string     | true |        课程总章节         |
|   `objective`    |    string     | true |     课程简介 (富文本)     |
|   `priceList`    |  list<price>  | true |           套餐            |
|  `teacherList`   | list<teacher> | true |           讲师            |

### priceList 详细

|     参数      |  类型  | 必填  |   描述    |
| :-----------: | :----: | :---: | :-------: |
|     `id`      | string | true  |  套餐 id  |
| `packageName` | string | true  | 套餐 名称 |
|    `type`     | string | false | 套餐 类型 |
|  `perPrice`   | double | true  | 套餐价格  |

### teacherList 详细

|      参数      |  类型  | 必填  |  描述   |
| :------------: | :----: | :---: | :-----: |
|      `id`      | string | true  | 讲师 id |
|     `name`     | string | true  |  姓名   |
| `introduction` | string | false |  介绍   |

## 返回格式

```js
data:
  {
    courseNumber: "112123",
    name: '课程名称11',
    isFineDesigned: 0,
    introduction: 20.0,
    videoPeriod: "1515",
    sectionAmount: "226",
    objective:'课程主要/。。。。',
    priceList: [{
      id:'',
      packageName:'',
      type:'',
      perPrice:''
    }],
    teacherList: [{
      id:'',
      name:'',
      introduction:'',
    }],
  },

```
