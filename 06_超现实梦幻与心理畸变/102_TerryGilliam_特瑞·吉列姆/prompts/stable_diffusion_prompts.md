# 特瑞·吉列姆 — Stable Diffusion 提示词

> 风格：反乌托邦荒诞、广角畸变、拼贴超现实、脏乱诗意

---

## 正向提示词（Positive）

```
cinematic, film still, in the style of TerryGilliam, 反乌托邦荒诞、广角畸变、拼贴超现实、脏乱诗意, 蒸汽朋克色, 脏乱质感, 高饱和点缀, 广角畸变, 拼贴美学, 反乌托邦 atmosphere, 低照度暖光、蒸汽朋克光、彩色色光、混乱光影, 35mm, film grain, depth of field, masterpiece, best quality
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
- **触发词**：`in the style of TerryGilliam`
