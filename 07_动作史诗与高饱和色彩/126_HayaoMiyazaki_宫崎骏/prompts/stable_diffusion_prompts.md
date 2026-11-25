# 宫崎骏 — Stable Diffusion 提示词

> 风格：手绘蓝天、飞行梦想、绿色自然、少女成长

---

## 正向提示词（Positive）

```
cinematic, film still, in the style of HayaoMiyazaki, 手绘蓝天、飞行梦想、绿色自然、少女成长, 吉卜力蓝, 自然绿, 手绘色彩, 飞行场景, 自然风景, 飞行梦想 atmosphere, 柔和天光、自然漫射、温暖阳光、梦幻光感, 35mm, film grain, depth of field, masterpiece, best quality
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
- **触发词**：`in the style of HayaoMiyazaki`
