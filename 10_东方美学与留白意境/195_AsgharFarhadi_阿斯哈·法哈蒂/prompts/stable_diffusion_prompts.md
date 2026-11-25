# 阿斯哈·法哈蒂 — Stable Diffusion 提示词

> 风格：道德悬疑、公寓内景、社会阶层、真实表演

---

## 正向提示词（Positive）

```
cinematic, film still, in the style of AsgharFarhadi, 道德悬疑、公寓内景、社会阶层、真实表演, 法哈蒂棕灰, 道德困境色, 伊朗公寓色, 公寓内景, 道德困境, 道德悬疑 atmosphere, 室内柔光、自然天光、公寓荧光、真实质感, 35mm, film grain, depth of field, masterpiece, best quality
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
- **触发词**：`in the style of AsgharFarhadi`
