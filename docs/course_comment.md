<!-- course_comment.md -->

# 课程的评论

?> 根据课程 id 查询课程评论。

|          接口名          | 请求方式 | 使用频率 |
| :----------------------: | :------: | :------: |
| `/public/course/comment` |   post   |   常用   |

## 请求参数

|      参数      |  类型  | 必填 |        描述        |
| :------------: | :----: | :--: | :----------------: |
| `courseNumber` | string | true | 课程 course_number |

## 返回参数

|     参数      | 类型 | 必填 |   描述   |
| :-----------: | :--: | :--: | :------: |
| `commentList` | list | true | 评论列表 |

### commentList 详细

|     参数      |  类型  | 必填 |   描述   |
| :-----------: | :----: | :--: | :------: |
|     `id`      | string | true | 评论 id  |
|    `score`    |  int   | true |   评分   |
|   `content`   | string | true |   内容   |
|  `createdBy`  | string | true |  用户名  |
| `createdDate` |  date  | true | 评论时间 |

## 返回格式

```js
data: [
  {
    id: "",
    score: "",
    content: "",
    createdBy: "",
    createdDate: "",
  },
  {
    id: "",
    score: "",
    content: "",
    createdBy: "",
    createdDate: "",
  },
];
```
