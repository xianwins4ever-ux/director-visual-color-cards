# 库布里克 — Stable Diffusion 提示词

> 风格：对称强迫、冷红蓝对比、广角畸变、凝视恐惧

---

## 正向提示词（Positive）

```
cinematic, film still, in the style of StanleyKubrick, 对称强迫、冷红蓝对比、广角畸变、凝视恐惧, 冷红蓝对比, 对称色光, 高饱和点缀, 对称强迫, 单点透视, 存在恐惧 atmosphere, 单点透视光、对称照明、冷色基调、高反差阴影, 35mm, film grain, depth of field, masterpiece, best quality
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
- **触发词**：`in the style of StanleyKubrick`
