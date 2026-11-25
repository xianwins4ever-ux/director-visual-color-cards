# 姆里纳尔·森 — Stable Diffusion 提示词

> 风格：印度新电影、政治激进、加尔各答街景、社会批判

---

## 正向提示词（Positive）

```
cinematic, film still, in the style of MrinalSen, 印度新电影、政治激进、加尔各答街景、社会批判, 姆里纳尔森黑白, 印度新电影色, 加尔各答棕调, 加尔各答街景, 政治主题, 政治激进 atmosphere, 街景自然光、高反差黑白、室内暖光、写实照明, 35mm, film grain, depth of field, masterpiece, best quality
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
- **触发词**：`in the style of MrinalSen`
