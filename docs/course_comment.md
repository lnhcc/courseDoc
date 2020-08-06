<!-- course_comment.md -->

# 课程的评论

?> 根据课程 id 查询课程评论。

|      接口名      | 请求方式 | 使用频率 |
| :--------------: | :------: | :------: |
| `course/comment` |   get    |   常用   |

## 请求参数

| 参数 |  类型  | 必填 |  描述   |
| :--: | :----: | :--: | :-----: |
| `id` | string | true | 课程 id |

## 返回参数

|         参数         | 类型 | 必填 |   描述   |
| :------------------: | :--: | :--: | :------: |
| `data <commentList>` | list | true | 评论列表 |

### commentList 详细

|    参数     |  类型  | 必填 |   描述   |
| :---------: | :----: | :--: | :------: |
| `commentId` | string | true | 评论 id  |
|   `count`   |  int   | true |   评分   |
|  `content`  | string | true |   内容   |
|   `name`    | string | true | 用户姓名 |
|  `picture`  | string | true | 用户头像 |
|   `time`    |  date  | true | 评论时间 |

## 返回格式

```js
data: [
  {
    commentId: "",
    count: "",
    content: "",
    name: "",
    picture: "",
    time: "",
  },
  {
    commentId: "",
    count: "",
    content: "",
    name: "",
    picture: "",
    time: "",
  },
];
```
