# LimeMqtt MQTT 通信

## 介绍

跨平台 MQTT 客户端，支持连接、订阅、发布、断开、消息监听、状态监听。支持安卓、iOS、鸿蒙 Next、Web、微信小程序。APP 需自定义基座。

**依赖：** 无

## 使用

```js
import { useMQTT } from '@/uni_modules/lime-mqtt'

const mqttClient = useMQTT()
mqttClient.connect({
  host: 'broker.example.com',
  port: 8083,
  clientId: 'myClient_123',
  username: 'user',
  password: 'pass',
  useSSL: true,
  reconnect: false,
  success(res) {},
  fail(err) {}
})
mqttClient.subscribe({ topic: 'home/sensor/temperature', qos: 1, success(res) {} })
mqttClient.unsubscribe({ topic: '...', success(res) {} })
mqttClient.publish({ topic: 'home/light/control', payload: 'turn_on', qos: 1 })
mqttClient.onMessage((msg) => { console.log(msg.topic, msg.payloadString) })
mqttClient.onStateChange((stateInfo) => {})
mqttClient.disconnect({ success(res) {} })
```

## API

useMQTT()。connect、disconnect、subscribe、unsubscribe、publish、onMessage、offMessage、onStateChange、offStateChange。isConnected。

## 插件入口

`lime-mqtt`：useMQTT
