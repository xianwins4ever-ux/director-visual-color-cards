# 奉俊昊 — Stable Diffusion 提示词

> 风格：阶级对比色、上下构图、黑色幽默、社会解剖

---

## 正向提示词（Positive）

```
cinematic, film still, in the style of BongJoon-ho, 阶级对比色、上下构图、黑色幽默、社会解剖, 寄生虫绿棕, 阶级对比色, 雨雾灰调, 上下构图, 阶级空间, 阶级批判 atmosphere, 冷暖对比光、地下室暗光、自然光、雨天灰光, 35mm, film grain, depth of field, masterpiece, best quality
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
- **触发词**：`in the style of BongJoon-ho`
