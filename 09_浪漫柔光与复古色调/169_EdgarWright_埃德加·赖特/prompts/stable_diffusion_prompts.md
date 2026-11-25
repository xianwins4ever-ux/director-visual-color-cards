# 埃德加·赖特 — Stable Diffusion 提示词

> 风格：快速剪辑、英式幽默、色彩分区、类型解构

---

## 正向提示词（Positive）

```
cinematic, film still, in the style of EdgarWright, 快速剪辑、英式幽默、色彩分区、类型解构, 埃德加赖特高饱和, 类型片色彩, 英式喜剧色, 快速剪辑, 类型解构, 英式幽默 atmosphere, 高饱和色光、类型片布光、快速切换光、漫画色光, 35mm, film grain, depth of field, masterpiece, best quality
```

## 负向提示词（Negative）

```
cartoon, anime, 3d render, low quality, blurry, distorted, overexposed, underexposed, ugly, deformed, bad anatomy, watermark, text, logo
```

---

## 参数设置

| 参数 | 推荐值 |
|------|--------|
| Sampler | DPM++ 2M Karras |
| Steps | 25-30 |
| CFG Scale | 7 |
| Resolution | 1024x576 (16:9) |
| Model | Realistic Vision / Deliberate |

---

## LoRA 训练建议

- **数据集**：50-100 张高清截图
- **标注**：导演风格 + 场景描述
- **训练轮数**：10-20 epochs
- **触发词**：`in the style of EdgarWright`
