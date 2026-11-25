# 河濑直美 — Stable Diffusion 提示词

> 风格：奈良绿光、自然母性、私小说电影、手持诗意

---

## 正向提示词（Positive）

```
cinematic, film still, in the style of NaomiKawase, 奈良绿光、自然母性、私小说电影、手持诗意, 河濑直美绿, 奈良森林色, 自然母性色, 自然森林, 母性主题, 自然母性 atmosphere, 森林绿光、自然柔光、丁达尔效应、晨昏光线, 35mm, film grain, depth of field, masterpiece, best quality
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
- **触发词**：`in the style of NaomiKawase`
