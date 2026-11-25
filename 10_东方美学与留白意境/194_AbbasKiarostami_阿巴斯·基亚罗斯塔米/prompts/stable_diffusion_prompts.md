# 阿巴斯·基亚罗斯塔米 — Stable Diffusion 提示词

> 风格：乡村公路、极简诗意、汽车对话、真假难辨

---

## 正向提示词（Positive）

```
cinematic, film still, in the style of AbbasKiarostami, 乡村公路、极简诗意、汽车对话、真假难辨, 阿巴斯金棕, 伊朗乡村色, 汽车对话色, 汽车内景, 乡村公路, 极简诗意 atmosphere, 自然光效、乡村阳光、车内柔光、伊朗高原光, 35mm, film grain, depth of field, masterpiece, best quality
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
- **触发词**：`in the style of AbbasKiarostami`
