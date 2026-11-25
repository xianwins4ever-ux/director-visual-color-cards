# 玛雅·德伦 — Stable Diffusion 提示词

> 风格：实验黑白、仪式舞蹈、诗意蒙太奇、梦的逻辑

---

## 正向提示词（Positive）

```
cinematic, film still, in the style of MayaDeren, 实验黑白、仪式舞蹈、诗意蒙太奇、梦的逻辑, 高反差黑白, 实验电影色, 16mm颗粒, 舞蹈身体, 多重曝光, 诗意实验 atmosphere, 高反差黑白、侧光雕刻、自然光、舞台光, 35mm, film grain, depth of field, masterpiece, best quality
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
- **触发词**：`in the style of MayaDeren`
