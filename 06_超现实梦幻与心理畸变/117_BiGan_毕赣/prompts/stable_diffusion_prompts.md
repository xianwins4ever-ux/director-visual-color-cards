# 毕赣 — Stable Diffusion 提示词

> 风格：梦境长镜头、贵州雨雾、霓虹诗意、时间迷宫

---

## 正向提示词（Positive）

```
cinematic, film still, in the style of BiGan, 梦境长镜头、贵州雨雾、霓虹诗意、时间迷宫, 贵州雨雾色, 霓虹粉蓝, 梦境色彩, 梦境长镜头, 贵州小镇, 时间迷宫 atmosphere, 霓虹色光、雨雾散射、暗调暖光、彩色灯串, 35mm, film grain, depth of field, masterpiece, best quality
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
- **触发词**：`in the style of BiGan`
