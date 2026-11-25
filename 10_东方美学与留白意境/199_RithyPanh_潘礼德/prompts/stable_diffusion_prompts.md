# 潘礼德 — Stable Diffusion 提示词

> 风格：红色高棉记忆、柬埔寨伤痕、纪录片式、儿童视角

---

## 正向提示词（Positive）

```
cinematic, film still, in the style of RithyPanh, 红色高棉记忆、柬埔寨伤痕、纪录片式、儿童视角, 潘礼德土黄, 柬埔寨伤痕色, 红色高棉色, 柬埔寨丛林, 红色高棉, 红色高棉记忆 atmosphere, 丛林绿光、土黄回忆、雨季灰光、蜡烛暖光, 35mm, film grain, depth of field, masterpiece, best quality
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
- **触发词**：`in the style of RithyPanh`
