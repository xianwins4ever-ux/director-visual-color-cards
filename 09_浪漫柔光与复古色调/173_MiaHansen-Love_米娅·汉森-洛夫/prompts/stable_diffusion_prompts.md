# 米娅·汉森-洛夫 — Stable Diffusion 提示词

> 风格：法国知性、时间流逝、人生岔路、柔光日常

---

## 正向提示词（Positive）

```
cinematic, film still, in the style of MiaHansen-Love, 法国知性、时间流逝、人生岔路、柔光日常, 汉森洛夫蓝绿, 法国知性色, 巴黎日常光, 巴黎街景, 人生岔路, 时间流逝 atmosphere, 巴黎自然光、柔光漫射、窗光侧光、真实色彩, 35mm, film grain, depth of field, masterpiece, best quality
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
- **触发词**：`in the style of MiaHansen-Love`
