# 乔安娜·霍格 — Stable Diffusion 提示词

> 风格：英国中产、自传色彩、静态构图、家具电影

---

## 正向提示词（Positive）

```
cinematic, film still, in the style of JoannaHogg, 英国中产、自传色彩、静态构图、家具电影, 乔安娜霍格暖棕, 英伦敦灰调, 中产阶级色, 静态构图, 英伦公寓, 英国中产 atmosphere, 室内柔光、英国阴天、自然窗光、暖色台灯, 35mm, film grain, depth of field, masterpiece, best quality
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
- **触发词**：`in the style of JoannaHogg`
