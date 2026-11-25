# 佐杜洛夫斯基 — Stable Diffusion 提示词

> 风格：炼金术色彩、宗教超现实、迷幻浓烈、神秘象征

---

## 正向提示词（Positive）

```
cinematic, film still, in the style of AlejandroJodorowsky, 炼金术色彩、宗教超现实、迷幻浓烈、神秘象征, 炼金术士色, 高饱和迷幻, 宗教色光, 宗教仪式, 神秘象征, 神秘主义 atmosphere, 色光照明、神圣光束、高饱和色光、仪式光影, 35mm, film grain, depth of field, masterpiece, best quality
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
- **触发词**：`in the style of AlejandroJodorowsky`
