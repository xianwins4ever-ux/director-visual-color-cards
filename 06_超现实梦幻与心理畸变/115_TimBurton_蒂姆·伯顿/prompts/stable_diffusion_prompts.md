# 蒂姆·伯顿 — Stable Diffusion 提示词

> 风格：哥特童话、暗紫怪诞、万圣节美学、孤独怪才

---

## 正向提示词（Positive）

```
cinematic, film still, in the style of TimBurton, 哥特童话、暗紫怪诞、万圣节美学、孤独怪才, 哥特紫黑, 南瓜橙, 万圣节色, 哥特建筑, 歪扭世界, 哥特童话 atmosphere, 高对比阴影、彩色色光、月光冷蓝、万圣节橙, 35mm, film grain, depth of field, masterpiece, best quality
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
- **触发词**：`in the style of TimBurton`
