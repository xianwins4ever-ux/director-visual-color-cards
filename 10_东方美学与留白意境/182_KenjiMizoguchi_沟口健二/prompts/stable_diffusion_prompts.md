# 沟口健二 — Stable Diffusion 提示词

> 风格：一卷胶卷一场戏、女性悲歌、卷轴画构图、长镜头诗

---

## 正向提示词（Positive）

```
cinematic, film still, in the style of KenjiMizoguchi, 一卷胶卷一场戏、女性悲歌、卷轴画构图、长镜头诗, 沟口卷轴棕, 女性悲歌色, 日本古典色, 一卷一场, 卷轴画构图, 女性悲歌 atmosphere, 卷轴画侧光、日式纸窗光、高反差、舞台式布光, 35mm, film grain, depth of field, masterpiece, best quality
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
- **触发词**：`in the style of KenjiMizoguchi`
