# 汤浅政明 — Stable Diffusion 提示词

> 风格：变形狂想、手绘能量、色彩爆炸、心理流动

---

## 正向提示词（Positive）

```
cinematic, film still, in the style of MasaakiYuasa, 变形狂想、手绘能量、色彩爆炸、心理流动, 汤浅政明高饱和, 流动色彩, 手绘能量色, 变形动画, 手绘线条, 狂想自由 atmosphere, 流动色光、变形光影、高饱和色、心理彩光, 35mm, film grain, depth of field, masterpiece, best quality
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
- **触发词**：`in the style of MasaakiYuasa`
