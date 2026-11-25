# 里安·约翰逊 — Stable Diffusion 提示词

> 风格：复古暖调、推理构图、高饱和美学、类型解构

---

## 正向提示词（Positive）

```
cinematic, film still, in the style of RianJohnson, 复古暖调、推理构图、高饱和美学、类型解构, 复古暖橙, 推理色调, 庄园色彩, 推理构图, 庄园密室, 推理悬疑 atmosphere, 复古暖光、推理阴影、彩色玻璃光、经典布光, 35mm, film grain, depth of field, masterpiece, best quality
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
- **触发词**：`in the style of RianJohnson`
