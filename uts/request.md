# LimeRequest 网络请求库

## 介绍

基于 uni.request 封装，支持拦截器、GET/POST/PUT/DELETE/HEAD/OPTIONS/TRACE/CONNECT、upload、download、baseURL、timeout、getTask 取消请求。除 upload/download 外需传泛型如 request.get&lt;T&gt;('/users')。

**依赖：** 无

## 使用

```js
import { Request } from '@/uni_modules/lime-request'

const request = new Request({
  baseURL: 'https://api.example.com',
  timeout: 10000,
  header: { 'Content-Type': 'application/json' }
})

request.get('/users', { params: { ID: 12345 } }).then(res => console.log(res.data))
request.post('/pet', { name: 'Hello', status: 'sold' }).then(res => {})
request.upload('/upload', { filePath: '/path/to/file.jpg', name: 'file', formData: {} })
request.download('/download', { filePath: '/storage/file.jpg' })

request.interceptors.request.use(config => config, err => Promise.reject(err))
request.interceptors.response.use(res => res, err => Promise.reject(err))
```

## API

new Request(config)。方法：request、get、post、put、delete、head、options、trace、connect、upload、download。interceptors.request.use、interceptors.response.use。LimeRequestConfig：baseURL、url、data、params、header、method、timeout、dataType、responseType、filePath、name、formData、getTask 等。

## 插件入口

`lime-request`：Request
