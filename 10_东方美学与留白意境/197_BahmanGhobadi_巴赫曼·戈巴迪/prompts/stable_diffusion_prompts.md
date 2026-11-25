# 巴赫曼·戈巴迪 — Stable Diffusion 提示词

> 风格：库尔德荒野、诗性纪录、音乐主题、边境故事

---

## 正向提示词（Positive）

```
cinematic, film still, in the style of BahmanGhobadi, 库尔德荒野、诗性纪录、音乐主题、边境故事, 戈巴迪金棕, 库尔德山野色, 诗性纪录色, 库尔德山区, 音乐主题, 库尔德身份 atmosphere, 荒野金光、自然天光、雪国冷光、山区侧光, 35mm, film grain, depth of field, masterpiece, best quality
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
- **触发词**：`in the style of BahmanGhobadi`
