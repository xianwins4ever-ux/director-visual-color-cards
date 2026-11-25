# 细田守 — Stable Diffusion 提示词

> 风格：数码世界、家庭温情、夏日青春、狼与龙

---

## 正向提示词（Positive）

```
cinematic, film still, in the style of MamoruHosoda, 数码世界、家庭温情、夏日青春、狼与龙, 细田守蓝, 夏日青春色, 数码世界光, 数码空间, 夏日乡村, 家庭温情 atmosphere, 数码蓝光、夏日阳光、家庭暖光、奇幻彩光, 35mm, film grain, depth of field, masterpiece, best quality
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
- **触发词**：`in the style of MamoruHosoda`
