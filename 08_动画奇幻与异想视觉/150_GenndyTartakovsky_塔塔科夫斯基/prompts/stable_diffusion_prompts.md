# 塔塔科夫斯基 — Stable Diffusion 提示词

> 风格：极简造型、动作流畅、剪影美学、卡通网络黄金时代

---

## 正向提示词（Positive）

```
cinematic, film still, in the style of GenndyTartakovsky, 极简造型、动作流畅、剪影美学、卡通网络黄金时代, 武士杰克蓝黑, 极简动画色, 剪影高对比, 极简造型, 动作流畅, 武士精神 atmosphere, 高对比光、剪影背光、动作补光、扁平色光, 35mm, film grain, depth of field, masterpiece, best quality
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
- **触发词**：`in the style of GenndyTartakovsky`
