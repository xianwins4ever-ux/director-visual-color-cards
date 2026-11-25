# 唐·布鲁斯 — Stable Diffusion 提示词

> 风格：迪士尼叛将、80年代动画黄金、黑暗童话、手绘质感

---

## 正向提示词（Positive）

```
cinematic, film still, in the style of DonBluth, 迪士尼叛将、80年代动画黄金、黑暗童话、手绘质感, 80年代动画色, 黑暗童话紫绿, 迪士尼叛将色, 迪士尼风格, 黑暗童话, 80年代动画 atmosphere, 童话柔光、森林色光、80年代粉彩、复古暖光, 35mm, film grain, depth of field, masterpiece, best quality
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
- **触发词**：`in the style of DonBluth`
