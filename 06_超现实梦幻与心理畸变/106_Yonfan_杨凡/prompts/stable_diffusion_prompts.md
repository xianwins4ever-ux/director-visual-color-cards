# 杨凡 — Stable Diffusion 提示词

> 风格：东方耽美、丝绸柔光、颓废美学、游园惊梦

---

## 正向提示词（Positive）

```
cinematic, film still, in the style of Yonfan, 东方耽美、丝绸柔光、颓废美学、游园惊梦, 东方耽美色, 丝绸柔光, 胭脂水粉, 丝绸质感, 镜面反射, 颓废美学 atmosphere, 柔光漫射、丝绸反光、烛光暖调、窗棂光影, 35mm, film grain, depth of field, masterpiece, best quality
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
- **触发词**：`in the style of Yonfan`
