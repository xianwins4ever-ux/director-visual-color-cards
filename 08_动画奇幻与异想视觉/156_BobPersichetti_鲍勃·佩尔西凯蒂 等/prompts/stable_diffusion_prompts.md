# 鲍勃·佩尔西凯蒂 等 — Stable Diffusion 提示词

> 风格：漫画美学、多元宇宙、赛博朋克、霓虹蛛网

---

## 正向提示词（Positive）

```
cinematic, film still, in the style of BobPersichetti, 漫画美学、多元宇宙、赛博朋克、霓虹蛛网, 平行宇宙色彩, 漫画美学色, 赛博霓虹色, 漫画分镜, 多元宇宙, 少年英雄 atmosphere, 霓虹色光、漫画网点、赛博朋克光、多元宇宙彩光, 35mm, film grain, depth of field, masterpiece, best quality
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
- **触发词**：`in the style of BobPersichetti`
