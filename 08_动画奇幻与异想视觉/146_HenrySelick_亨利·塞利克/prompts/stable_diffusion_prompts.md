# 亨利·塞利克 — Stable Diffusion 提示词

> 风格：定格暗黑童话、万圣节美学、哥特奇幻、蒂姆伯顿搭档

---

## 正向提示词（Positive）

```
cinematic, film still, in the style of HenrySelick, 定格暗黑童话、万圣节美学、哥特奇幻、蒂姆伯顿搭档, 万圣节橙紫, 定格暗黑色, 哥特童话色, 定格动画, 万圣节镇, 黑暗童话 atmosphere, 月光冷光、南瓜暖光、哥特暗影、童话色光, 35mm, film grain, depth of field, masterpiece, best quality
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
- **触发词**：`in the style of HenrySelick`
