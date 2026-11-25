# 弗朗索瓦·特吕弗 — Stable Diffusion 提示词

> 风格：新浪潮旗手、四百击少年、安托万系列、浪漫怀旧

---

## 正向提示词（Positive）

```
cinematic, film still, in the style of FrancoisTruffaut, 新浪潮旗手、四百击少年、安托万系列、浪漫怀旧, 新浪潮黑白, 特吕弗暖调, 巴黎棕黄, 四百击定格, 安托万系列, 新浪潮 atmosphere, 黑白高对比、彩色暖调、巴黎街光、柔光漫射, 35mm, film grain, depth of field, masterpiece, best quality
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
- **触发词**：`in the style of FrancoisTruffaut`
