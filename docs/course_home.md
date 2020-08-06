<!-- course_home.md -->

# 首页课程（后做）

?> 首页课程列表。返回三个分类，每个分类下五个课程。

|    接口名     | 请求方式 | 使用频率 |
| :-----------: | :------: | :------: |
| `course/home` |   get    |   常用   |

## 请求参数

| 参数 | 类型 | 必填 | 描述 |
| :--: | :--: | :--: | :--: |
|  无  |      |      |      |

## 返回参数

|        参数         | 类型 | 必填 |   描述   |
| :-----------------: | :--: | :--: | :------: |
| `data <ColumnList>` | list | true | 分类数组 |

### ColumnList 详细

|        参数         |  类型  | 必填 |   描述   |
| :-----------------: | :----: | :--: | :------: |
|        name         | string | true | 分类名称 |
| `list <CourseList>` |  list  | true | 课程数组 |

### CourseList 详细

|       参数       |  类型  | 必填 |           描述            |
| :--------------: | :----: | :--: | :-----------------------: |
|    `courseId`    | string | true |          课程 id          |
|   `courseName`   | string | true |         课程名称          |
|   `courseType`   |  int   | true | 课程标签（0 普通 1 精品） |
|  `coursePrice`   | double | true |         课程售价          |
| `courseDuration` |  int   | true |      课程时长 (min)       |
| `courseSection`  |  int   | true |        课程总章节         |

## 返回格式

```js
data: [{
	name: '分类一'，
	list: [{
			courseId:'',
			courseName: "课程名称12",
    		courseType: 0,
    		coursePrice: 10.0,
    		courseDuration: 20,
    		courseSection: 10,
		},
		{
			courseId:'',
			courseName: "课程名称12",
    		courseType: 0,
    		coursePrice: 10.0,
   		 	courseDuration: 20,
    		courseSection: 10,
		}
	]
}, {
	name: '分类二'，
	list: [{
		courseId:'',
		courseName: "课程名称12",
    	courseType: 0,
    	coursePrice: 10.0,
    	courseDuration: 20,
    	courseSection: 10,
	}]
}]

```
