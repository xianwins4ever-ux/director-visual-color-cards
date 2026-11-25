# 米歇尔·冈瑞 — Stable Diffusion 提示词

> 风格：手工特效、微缩梦幻、DIY超现实、情感纯真

---

## 正向提示词（Positive）

```
cinematic, film still, in the style of MichelGondry, 手工特效、微缩梦幻、DIY超现实、情感纯真, 粉彩梦境, 低饱和柔光, 手工质感, 微缩模型, 分屏画面, 纯真忧伤 atmosphere, 柔光漫射、彩色灯光、自然光、DIY光影, 35mm, film grain, depth of field, masterpiece, best quality
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
- **触发词**：`in the style of MichelGondry`
