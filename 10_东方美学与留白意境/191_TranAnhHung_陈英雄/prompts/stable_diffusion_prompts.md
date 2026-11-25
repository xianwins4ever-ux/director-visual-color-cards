# 陈英雄 — Stable Diffusion 提示词

> 风格：越南绿意、美食光影、法式诗意、东方含蓄

---

## 正向提示词（Positive）

```
cinematic, film still, in the style of TranAnhHung, 越南绿意、美食光影、法式诗意、东方含蓄, 陈英雄绿金, 青木瓜色, 越南美食色, 越南风景, 美食光影, 越南诗意 atmosphere, 柔光漫射、窗格光影、自然天光、食物暖光, 35mm, film grain, depth of field, masterpiece, best quality
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
- **触发词**：`in the style of TranAnhHung`
