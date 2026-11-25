# 大岛渚 — Stable Diffusion 提示词

> 风格：禁忌色彩、东方肉体、极端美学、政治情欲

---

## 正向提示词（Positive）

```
cinematic, film still, in the style of NagisaOshima, 禁忌色彩、东方肉体、极端美学、政治情欲, 血樱红, 日式纸窗光, 禁忌色, 日式空间, 身体特写, 禁忌之爱 atmosphere, 高对比暖光、红色重点光、日式纸窗光、暗调阴影, 35mm, film grain, depth of field, masterpiece, best quality
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
- **触发词**：`in the style of NagisaOshima`
