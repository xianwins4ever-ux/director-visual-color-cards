# 克莱尔·德尼 — Stable Diffusion 提示词

> 风格：非洲记忆、身体感官、极简叙事、诗意留白

---

## 正向提示词（Positive）

```
cinematic, film still, in the style of ClaireDenis, 非洲记忆、身体感官、极简叙事、诗意留白, 德尼金棕, 非洲记忆色, 身体感官色, 身体特写, 非洲记忆, 身体政治 atmosphere, 非洲金光、皮肤侧光、暗调阴影、自然柔光, 35mm, film grain, depth of field, masterpiece, best quality
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
- **触发词**：`in the style of ClaireDenis`
