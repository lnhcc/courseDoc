<!-- course_home.md -->

# 首页课程

?> 首页课程列表。返回三个分类，每个分类下五个课程。

|    接口名     | 请求方式 | 使用频率 |
| :-----------: | :------: | :------: |
| `course/home` |   get    |   常用   |

## 请求参数

|  参数  |  类型  | 必填  |      描述       |
| :----: | :----: | :---: | :-------------: |
| `test` | string | false | 测试参数 啊啊啊 |

## 返回参数

|        参数         | 类型 | 必填 |   描述   |
| :-----------------: | :--: | :--: | :------: |
| `data <ColumnList>` | list | true | 分类数组 |

## ColumnList 详细

|        参数         |  类型  | 必填 |   描述   |
| :-----------------: | :----: | :--: | :------: |
|        name         | string | true | 分类名称 |
| `list <CourseList>` |  list  | true | 课程数组 |

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
data: [{
	name: '分类一'，
	list: [{
			courseName: '课程名称11',
			coursePrice: 10.00,
			courseWatchCount: 20,
			courseSaleCount: 1,
		},
		{
			courseName: '课程名称12',
			coursePrice: 10.00,
			courseWatchCount: 20,
			courseSaleCount: 1,
		}
	]
}, {
	name: '分类二'，
	list: [{
		courseName: '课程名称21',
		coursePrice: 10.00,
		courseWatchCount: 20,
		courseSaleCount: 1,
	}]
}]

```
