# LimeColor 颜色工具

## 介绍

颜色解析、转换、修改、组合工具。支持 HEX、RGB、HSL、HSV、颜色名、数字等输入；toHsv/toHsl/toHex/toRgb/toName；lighten、darken、saturate、spin、mix；analogous、monochromatic、triad、tetrad、complement；generate 主题色。基于 tinycolor 思路。

**依赖：** 无

## 使用

```js
import { tinyColor } from '@/uni_modules/lime-color'
import { generate } from '@/uni_modules/lime-color'

const color = tinyColor('#f00')
color.toHexString()
color.toRgb()
color.lighten(10).toString()
color.darken(10).saturate(20).spin(180)
color.mix(tinyColor('#0f0'), 50)
tinyColor('#f00').analogous().map(t => t.toHexString())
tinyColor('#f00').complement().toHexString()
generate('red')
generate('red', { theme: 'dark' })
```

## API

tinyColor(color, opts)：解析多种格式，返回实例。实例：toHsv/toHsl/toHex/toRgb/toName、lighten/brighten/darken/tint/shade、desaturate/saturate/greyscale、spin、mix、analogous/monochromatic/triad/tetrad/complement、getBrightness/isLight/isDark、getAlpha/setAlpha、clone/equals。generate(color, options)：生成主题色数组。

## 插件入口

`lime-color`：tinyColor、generate
