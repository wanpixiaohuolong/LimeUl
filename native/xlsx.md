# LimeXlsx Excel 与 JSON

## 介绍

Excel(.xlsx，安卓还支持 .xls) 与 JSON 互转。支持 IOS/Android/Web/鸿蒙 Next/小程序。默认第一行为表头，读取第一个表。需自定义基座。

**依赖：** 无

## 使用

```js
import { excelToJson, jsonToExcel, type XlsxOptions } from '@/uni_modules/lime-xlsx'

excelToJson({
  path: '/static/example.xlsx',
  success(res) { console.log(res.data) },
  fail(err) {}
})
jsonToExcel({
  json: JSON.stringify([{ name: 'Alice', age: 30 }]),
  success(res) { console.log(res.tempFilePath) },
  fail(err) {}
})
```

## API

excelToJson(options)：path、success、fail。jsonToExcel(options)：json 或 path、success、fail。

## 插件入口

`lime-xlsx`：excelToJson、jsonToExcel
