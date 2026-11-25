# 瑟琳·席安玛 — Stable Diffusion 提示词

> 风格：女同凝视、水彩柔光、肖像油画、时间温柔

---

## 正向提示词（Positive）

```
cinematic, film still, in the style of CelineSciamma, 女同凝视、水彩柔光、肖像油画、时间温柔, 肖像油画色, 水彩柔调, 女同电影色, 女性凝视, 肖像油画, 女性凝视 atmosphere, 油画侧光、窗光漫射、自然柔光、烛光辉映, 35mm, film grain, depth of field, masterpiece, best quality
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
- **触发词**：`in the style of CelineSciamma`
