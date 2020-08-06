<!-- index_ke.md -->

## 接口地址

| host       | http://192.168.141.143:10000 |
| ---------- | :--------------------------: |
| `basePath` |         /marketadmin         |

## 请求状态 code

| code （int 类型） |       状态码描述       |
| :---------------: | :--------------------: |
|       `200`       |          正常          |
|       `401`       |         未登录         |
|       `402`       |         未注册         |
|     `其他值`      | 异常(msg 返回错误原因) |

## 分页

?> 如果返回的是数据是 list,并且需要分页的时候。

### 请求参数

|  参数  | 类型 | 必填  |    描述    |
| :----: | :--: | :---: | :--------: |
| `size` | int  | false | 每页数据数 |
| `page` | int  | false |  当前页码  |

### 返回参数

|         参数          |  类型  | 必填 |     描述      |
| :-------------------: | :----: | :--: | :-----------: |
|        `code`         |  int   | true | 0 异常 1 正常 |
|         `msg`         | string | true |     描述      |
|      `pageable`       |  obj   | true |   分页详情    |
|  `pageable.pageSize`  |  int   | true |  每页数据数   |
| `pageable.pageNumber` |  int   | true |   当前页码    |
|    `totalElements`    |  int   | true |   数据总数    |
|     `totalPages`      |  int   | true |    总页数     |
|        `data`         |  obj   | true |     信息      |

## 返回格式

```js
data:{
  code:1,
  msg:'正常',
  pageable:{
    pageNumber:1,
    pageSize:10,
  },
  totalElements:100,
  totalPages:10,
  data:{}
}

```
