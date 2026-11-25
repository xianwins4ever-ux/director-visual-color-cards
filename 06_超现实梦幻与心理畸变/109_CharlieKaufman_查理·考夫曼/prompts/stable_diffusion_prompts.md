# 查理·考夫曼 — Stable Diffusion 提示词

> 风格：元叙事迷宫、心理空间、意识流视觉、存在焦虑

---

## 正向提示词（Positive）

```
cinematic, film still, in the style of CharlieKaufman, 元叙事迷宫、心理空间、意识流视觉、存在焦虑, 心理冷调, 纽约灰蓝, 意识流色彩, 元叙事, 心理空间, 存在焦虑 atmosphere, 冷调自然光、室内荧光、心理色光、雨雾天, 35mm, film grain, depth of field, masterpiece, best quality
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
- **触发词**：`in the style of CharlieKaufman`
