# LimeSqlite SQLite 数据库

## 介绍

参考 plus.sqlite 的 SQLite UTS API，兼容 UniAppX（安卓、iOS、鸿蒙 Next）。打开/关闭/事务/执行 SQL/查询。鸿蒙不支持路径打开；Web 路径方式数据不存文件；iOS Windows 开发需自定义基座。

**依赖：** 付费插件

## 使用

```js
import { openDatabase, closeDatabase, isOpenDatabase, transaction, executeSql, selectSql, getDatabasePath } from '@/uni_modules/lime-sqlite'

openDatabase({ name: 'text', success(res) {}, fail(err) {} })
isOpenDatabase({ name: 'text', success(res) {} })
closeDatabase({ name: 'text', success(res) {} })
transaction({ name: 'text', operation: 'begin'|'commit'|'rollback', success(res) {} })
executeSql({ name: 'text', sql: ['CREATE TABLE...', 'INSERT...'], success(res) {} })
selectSql({ name: 'text', sql: ['SELECT * FROM test'], success(res) {} })
getDatabasePath('text')
```

## API

openDatabase、isOpenDatabase、closeDatabase(DatabaseOptions：name、path、success、fail)。transaction(SqlTransactionOptions：name、operation)。executeSql、selectSql(SqlOperationOptions：name、sql[]、success、fail)。getDatabasePath(name)。

## 插件入口

`lime-sqlite`：openDatabase、closeDatabase、isOpenDatabase、transaction、executeSql、selectSql、getDatabasePath
