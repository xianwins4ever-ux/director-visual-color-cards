# 今敏 — Stable Diffusion 提示词

> 风格：现实与梦交界、心理空间、剪辑魔法、女性主角

---

## 正向提示词（Positive）

```
cinematic, film still, in the style of SatoshiKon, 现实与梦交界、心理空间、剪辑魔法、女性主角, 今敏粉紫, 梦境色彩, 都市霓虹, 蒙太奇剪辑, 现实梦境交融, 心理迷宫 atmosphere, 柔光现实、梦境彩光、城市霓虹、室内暖光, 35mm, film grain, depth of field, masterpiece, best quality
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
- **触发词**：`in the style of SatoshiKon`
