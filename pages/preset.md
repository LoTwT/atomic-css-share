# Preset Demo

Unocss 因为[硬编码](https://github.com/unocss/unocss/blob/59e6c343d5645d547349721e9abfc5bb62ecdd80/packages/preset-mini/src/_utils/handlers/handlers.ts#L54)致使 `p-1` 在转换后是 `padding: 0.25rem`，这在有时候并不方便；以下是一个成倍放大基础 `0.25` 单位的预设，例如倍数是 `4` 时，`p-1` 将被转换为 `padding: 1rem`。

```ts{3,11-19}
import type { Preset } from "unocss"

const remRE = /^-?[\.\d]+rem$/

export default function presetRemTransform(multiplier = 1): Preset {
  if (multiplier <= 0) {
    throw new Error("unocss-preset-rem-transform: multiplier must be greater than 0 !")
  }
  return {
    name: "unocss-preset-rem-transform",
    postprocess: (util) => {
      util.entries.forEach((i) => {
        // i -> CSSEntry tuple [key, value] -> [string, string | number | undefined]
        // eg. [ "padding", "1rem" ] / [ "text-align", "center" ]
        const value = i[1]
        if (value && typeof value === "string" && remRE.test(value))
          i[1] = `${+value.slice(0, -3) * multiplier}rem`
      })
    },
  }
}
```
