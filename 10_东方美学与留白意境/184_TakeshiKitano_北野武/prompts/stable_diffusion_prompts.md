# 北野武 — Stable Diffusion 提示词

> 风格：暴力静帧、蓝色调、黑帮美学、死面表情

---

## 正向提示词（Positive）

```
cinematic, film still, in the style of TakeshiKitano, 暴力静帧、蓝色调、黑帮美学、死面表情, 北野蓝, 暴力静帧色, 黑帮蓝色调, 静止画面, 海边场景, 暴力美学 atmosphere, 海边冷光、蓝色色光、高反差、静止画面, 35mm, film grain, depth of field, masterpiece, best quality
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
- **触发词**：`in the style of TakeshiKitano`
