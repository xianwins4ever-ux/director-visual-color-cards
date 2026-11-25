# 伊日·特尔恩卡 — Stable Diffusion 提示词

> 风格：木偶动画之父、东欧诗意、捷克制图、童话暗黑

---

## 正向提示词（Positive）

```
cinematic, film still, in the style of JiriTrnka, 木偶动画之父、东欧诗意、捷克制图、童话暗黑, 木偶棕褐色, 捷克灰调, 舞台金光, 木偶造型, 舞台构图, 木偶动画 atmosphere, 舞台式布光、木偶侧光、木质感光、暗调阴影, 35mm, film grain, depth of field, masterpiece, best quality
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
- **触发词**：`in the style of JiriTrnka`
