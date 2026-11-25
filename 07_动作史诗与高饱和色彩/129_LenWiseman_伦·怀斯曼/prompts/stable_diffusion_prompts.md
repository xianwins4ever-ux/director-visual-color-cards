# 伦·怀斯曼 — Stable Diffusion 提示词

> 风格：蓝冷动作、地下世界、吸血鬼狼人、高饱和对比

---

## 正向提示词（Positive）

```
cinematic, film still, in the style of LenWiseman, 蓝冷动作、地下世界、吸血鬼狼人、高饱和对比, 暗夜蓝调, 血红点缀, 地下冷色, 地下世界, 吸血鬼狼人, 地下世界 atmosphere, 冷蓝月光、血色暖光、地下荧光、雨夜景, 35mm, film grain, depth of field, masterpiece, best quality
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
- **触发词**：`in the style of LenWiseman`
