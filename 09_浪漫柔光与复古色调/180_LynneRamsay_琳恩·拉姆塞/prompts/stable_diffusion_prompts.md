# 琳恩·拉姆塞 — Stable Diffusion 提示词

> 风格：暴力诗意、红色意象、主观视角、碎片叙事

---

## 正向提示词（Positive）

```
cinematic, film still, in the style of LynneRamsay, 暴力诗意、红色意象、主观视角、碎片叙事, 拉姆塞血红, 暴力诗意思, 主观碎片色, 主观视角, 碎片叙事, 暴力诗意 atmosphere, 高对比色光、红色重点光、暗调阴影、主观光效, 35mm, film grain, depth of field, masterpiece, best quality
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
- **触发词**：`in the style of LynneRamsay`
