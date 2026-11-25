# 肯尼斯·安格 — Stable Diffusion 提示词

> 风格：地下电影、霓虹迷幻、8mm颗粒、酷儿神话

---

## 正向提示词（Positive）

```
cinematic, film still, in the style of KennethAnger, 地下电影、霓虹迷幻、8mm颗粒、酷儿神话, 霓虹迷幻色, 8mm颗粒感, 酷儿霓虹, 地下电影, 8mm颗粒, 酷儿先锋 atmosphere, 霓虹色光、火焰光、月光冷蓝、彩色色片, 35mm, film grain, depth of field, masterpiece, best quality
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
- **触发词**：`in the style of KennethAnger`
