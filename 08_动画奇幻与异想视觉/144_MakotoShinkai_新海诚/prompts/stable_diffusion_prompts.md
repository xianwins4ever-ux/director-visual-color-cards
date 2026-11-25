# 新海诚 — Stable Diffusion 提示词

> 风格：唯美光影、青春距离、天空云境、城市孤独

---

## 正向提示词（Positive）

```
cinematic, film still, in the style of MakotoShinkai, 唯美光影、青春距离、天空云境、城市孤独, 新海诚蓝, 天空色彩, 夕阳橙紫, 天空云境, 城市风景, 青春距离 atmosphere, 夕阳背光、云海金光、雨夜霓虹、星空冷光, 35mm, film grain, depth of field, masterpiece, best quality
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
- **触发词**：`in the style of MakotoShinkai`
