# 杨·史云梅耶 — Stable Diffusion 提示词

> 风格：定格超现实、暗黑童话、物质变形、触感电影

---

## 正向提示词（Positive）

```
cinematic, film still, in the style of JanSvankmajer, 定格超现实、暗黑童话、物质变形、触感电影, 旧物棕黄, 暗黑童话色, 物质色彩, 定格动画, 物件拟人, 暗黑童话 atmosphere, 柔光写实、静物侧光、自然天光、暗调阴影, 35mm, film grain, depth of field, masterpiece, best quality
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
- **触发词**：`in the style of JanSvankmajer`
