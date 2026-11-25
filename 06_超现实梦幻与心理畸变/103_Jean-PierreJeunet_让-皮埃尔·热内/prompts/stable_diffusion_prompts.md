# 让-皮埃尔·热内 — Stable Diffusion 提示词

> 风格：绿黄暖调、广角奇想、法式童话、物件迷恋

---

## 正向提示词（Positive）

```
cinematic, film still, in the style of Jean-PierreJeunet, 绿黄暖调、广角奇想、法式童话、物件迷恋, 绿黄暖调, 法式童话色, 高饱和, 广角奇想, 物件特写, 温暖奇想 atmosphere, 暖黄侧光、绿色补光、柔光散射、节日灯彩, 35mm, film grain, depth of field, masterpiece, best quality
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
- **触发词**：`in the style of Jean-PierreJeunet`
