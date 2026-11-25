# 高畑勋 — Stable Diffusion 提示词

> 风格：写实水彩、社会写实、平民史诗、自然主义

---

## 正向提示词（Positive）

```
cinematic, film still, in the style of IsaoTakahata, 写实水彩、社会写实、平民史诗、自然主义, 吉卜力写实色, 水彩质感色, 平民棕绿, 水彩质感, 平民生活, 社会写实 atmosphere, 自然天光、柔和散射、水彩质感、生活气息, 35mm, film grain, depth of field, masterpiece, best quality
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
- **触发词**：`in the style of IsaoTakahata`
