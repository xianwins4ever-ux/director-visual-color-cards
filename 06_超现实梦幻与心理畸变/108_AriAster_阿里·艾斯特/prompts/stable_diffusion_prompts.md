# 阿里·艾斯特 — Stable Diffusion 提示词

> 风格：日光恐怖、民俗暖色、明亮中的恐惧、家庭创伤

---

## 正向提示词（Positive）

```
cinematic, film still, in the style of AriAster, 日光恐怖、民俗暖色、明亮中的恐惧、家庭创伤, 日光恐怖色, 民俗暖黄, 木屋棕调, 对称构图, 家庭空间, 日光恐怖 atmosphere, 自然日光、暖色火光、室内柔光、对比阴影, 35mm, film grain, depth of field, masterpiece, best quality
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
- **触发词**：`in the style of AriAster`
