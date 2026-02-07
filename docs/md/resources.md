# 资源包
资源包包含纹理、音效等资源。

::: warning
本页面的内容处于早期阶段，随时可能会修改。
:::

## 结构
```
.
├── shaders                     # 着色器文件夹
│   ├── rect                    # 渲染矩形着色器
│   │   ├── rect.vert           # 顶点着色器
│   │   └── rect.frag           # 片元着色器
│   ├── texture                 # 渲染纹理着色器
│   │   ├── texture.vert
│   └   └── texture.frag
├── sounds                      # 音效文件夹
│   ├── tap.ogg
│   ├── drag.ogg
│   └── flick.ogg
├── textures                    # 纹理文件夹
│   ├── notes                   # Note 纹理文件夹
│   │   ├── tap.png
│   │   ├── drag.png
│   │   ├── flick.png
│   │   ├── hold-bottom.png
│   │   ├── hold-middle.png
│   └   └── hold-top.png
└── config.toml                 # 配置文件
```

- 音频文件必须为 `*.ogg` 格式。
- 图片文件必须为 `*.png` 格式。

## 配置文件
- colors `table` : 颜色相关配置。
    - line_color `array` : 判定线颜色。

::: tip
- 所有颜色配置项均为三项的数组，分别表示 `R`、`G`、`B` ，每一项的值必须在 `0.0 - 1.0` 范围内。
:::

::: details 查看默认配置文件
``` toml
[colors]
line_color = [0.996078431372549, 1, 0.662745098039216]

```
:::

## 自定义资源包
- 你可以使用 `--resources-dir` 参数来指定资源包的路径。暂不支持压缩包。