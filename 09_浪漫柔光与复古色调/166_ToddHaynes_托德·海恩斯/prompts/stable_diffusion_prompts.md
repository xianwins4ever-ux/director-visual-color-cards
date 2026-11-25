# 托德·海恩斯 — Stable Diffusion 提示词

> 风格：道格拉斯色、酷儿美学、70年代复古、身份政治

---

## 正向提示词（Positive）

```
cinematic, film still, in the style of ToddHaynes, 道格拉斯色、酷儿美学、70年代复古、身份政治, 道格拉斯色, 70年代复古色, 酷儿紫粉, 道格拉斯色系, 70年代复古, 酷儿美学 atmosphere, 70年代暖光、道格拉斯色光、柔光镜头、复古色彩, 35mm, film grain, depth of field, masterpiece, best quality
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
- **触发词**：`in the style of ToddHaynes`
