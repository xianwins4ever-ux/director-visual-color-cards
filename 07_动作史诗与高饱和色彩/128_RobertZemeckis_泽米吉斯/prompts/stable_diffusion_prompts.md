# 泽米吉斯 — Stable Diffusion 提示词

> 风格：时空穿越、美式怀旧、技术先锋、温情奇幻

---

## 正向提示词（Positive）

```
cinematic, film still, in the style of RobertZemeckis, 时空穿越、美式怀旧、技术先锋、温情奇幻, 时光橙金, 科技蓝, 美式怀旧色, 时空穿越, 美式小镇, 时光旅行 atmosphere, 暖金怀旧光、科技蓝光、自然光、童话柔光, 35mm, film grain, depth of field, masterpiece, best quality
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
- **触发词**：`in the style of RobertZemeckis`
