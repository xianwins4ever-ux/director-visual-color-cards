# 彼特·道格特 — Stable Diffusion 提示词

> 风格：皮克斯情感、抽象概念可视化、温暖治愈、灵魂色彩

---

## 正向提示词（Positive）

```
cinematic, film still, in the style of PeteDocter, 皮克斯情感、抽象概念可视化、温暖治愈、灵魂色彩, 皮克斯暖调, 灵魂色彩, 情感粉彩, 抽象概念, 情感拟人, 情感探索 atmosphere, 柔光暖光、灵魂彩光、梦幻光感、自然天光, 35mm, film grain, depth of field, masterpiece, best quality
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
- **触发词**：`in the style of PeteDocter`
