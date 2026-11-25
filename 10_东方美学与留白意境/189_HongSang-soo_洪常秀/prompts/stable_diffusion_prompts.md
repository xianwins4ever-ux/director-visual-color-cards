# 洪常秀 — Stable Diffusion 提示词

> 风格：日常对话、黑白/淡彩、酒馆男女、结构游戏

---

## 正向提示词（Positive）

```
cinematic, film still, in the style of HongSang-soo, 日常对话、黑白/淡彩、酒馆男女、结构游戏, 洪常秀黑白, 酒馆棕调, 日常对话色, 酒馆场景, 男女对话, 日常对话 atmosphere, 自然光效、室内暖光、街景柔光、极简照明, 35mm, film grain, depth of field, masterpiece, best quality
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
- **触发词**：`in the style of HongSang-soo`
