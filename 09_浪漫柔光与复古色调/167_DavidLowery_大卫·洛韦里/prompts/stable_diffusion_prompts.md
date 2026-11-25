# 大卫·洛韦里 — Stable Diffusion 提示词

> 风格：诗意慢节奏、复古暖调、幽灵浪漫、德州光

---

## 正向提示词（Positive）

```
cinematic, film still, in the style of DavidLowery, 诗意慢节奏、复古暖调、幽灵浪漫、德州光, 大卫洛韦里暖金, 德州大地色, 幽灵灰调, 幽灵视角, 德州风光, 诗意慢电影 atmosphere, 黄金时刻、暖金柔光、烛光室内、自然天光, 35mm, film grain, depth of field, masterpiece, best quality
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
- **触发词**：`in the style of DavidLowery`
