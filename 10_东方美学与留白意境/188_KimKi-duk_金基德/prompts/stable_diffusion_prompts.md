# 金基德 — Stable Diffusion 提示词

> 风格：水与岛、沉默暴力、佛教意象、极端美学

---

## 正向提示词（Positive）

```
cinematic, film still, in the style of KimKi-duk, 水与岛、沉默暴力、佛教意象、极端美学, 金基德水色, 寺庙绿棕, 沉默暴力色, 水与岛, 寺庙漂浮, 沉默暴力 atmosphere, 水光反射、自然天光、寺庙暖光、冷调水面, 35mm, film grain, depth of field, masterpiece, best quality
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
- **触发词**：`in the style of KimKi-duk`
