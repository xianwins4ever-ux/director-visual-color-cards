# 杨德昌 — Stable Diffusion 提示词

> 风格：都市疏离、冷调构图、台北中产、长镜头观察

---

## 正向提示词（Positive）

```
cinematic, film still, in the style of EdwardYang, 都市疏离、冷调构图、台北中产、长镜头观察, 杨德昌冷灰, 台北都巿色, 中产棕调, 都市空间, 中产阶级, 都市疏离 atmosphere, 冷白荧光、玻璃窗光、都市霓虹、自然光, 35mm, film grain, depth of field, masterpiece, best quality
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
- **触发词**：`in the style of EdwardYang`
