# LimePrinter 打印

## 介绍

UTS 通过蓝牙/网络/USB 连接打印机发送指令(小票、标签)。目前主要测了安卓蓝牙(TSC)。需自定义基座。

**依赖：** 付费插件

## 使用

```js
import { usePrinter } from '@/uni_modules/lime-printer'

const printer = usePrinter()
printer.setUpConnection('bluetooth')  // 'net' | 'usb'
printer.search({ success() {}, fail(err) {} })
printer.onSearch((bt) => { console.log(bt.name, bt.deviceId) })
printer.connect({ deviceId: '...', success() {}, fail() {} })
printer.print({ data: 'SIZE 40 mm...\r\nPRINT 1,2\r\n' })
printer.stop()
printer.disconnect()
```

## API

usePrinter()。setUpConnection(type)。search(SearchOption)、onSearch(callback)、connect(ConnectOption)、print(PrintOption)、stop、disconnect。

## 插件入口

`lime-printer`：usePrinter
