# 大卫·雷奇 — Stable Diffusion 提示词

> 风格：高饱和动作、色彩分区、格斗美学、冷幽默

---

## 正向提示词（Positive）

```
cinematic, film still, in the style of DavidLeitch, 高饱和动作、色彩分区、格斗美学、冷幽默, 高饱和动作色, 色彩分区美学, 霓虹色光, 色彩分区, 格斗特写, 动作美学 atmosphere, 霓虹色光、分区色光、动作补光、高对比照明, 35mm, film grain, depth of field, masterpiece, best quality
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
- **触发词**：`in the style of DavidLeitch`
