# 黑泽清 — Stable Diffusion 提示词

> 风格：都市恐怖、空间异化、绿色诡异、静止长镜

---

## 正向提示词（Positive）

```
cinematic, film still, in the style of KiyoshiKurosawa, 都市恐怖、空间异化、绿色诡异、静止长镜, 黑泽清绿, 都市恐怖色, 空间异调色, 静止长镜, 空间异化, 都市恐怖 atmosphere, 荧光冷光、绿色色光、暗调阴影、都市霓虹, 35mm, film grain, depth of field, masterpiece, best quality
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
- **触发词**：`in the style of KiyoshiKurosawa`
