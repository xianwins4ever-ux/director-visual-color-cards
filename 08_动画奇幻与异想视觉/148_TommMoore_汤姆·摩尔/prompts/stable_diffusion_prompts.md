# 汤姆·摩尔 — Stable Diffusion 提示词

> 风格：凯尔经风格、凯尔特神话、平面装饰、手绘灵魂

---

## 正向提示词（Positive）

```
cinematic, film still, in the style of TommMoore, 凯尔经风格、凯尔特神话、平面装饰、手绘灵魂, 凯尔经色彩, 爱尔兰绿金, 凯尔特装饰色, 平面装饰, 凯尔特图案, 凯尔特神话 atmosphere, 教堂彩光、森林柔光、黄金时刻、烛光暖光, 35mm, film grain, depth of field, masterpiece, best quality
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
- **触发词**：`in the style of TommMoore`
