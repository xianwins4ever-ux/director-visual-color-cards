# 马修·巴尼 — Stable Diffusion 提示词

> 风格：行为艺术影像、身体雕塑、极端美学、悬丝系列

---

## 正向提示词（Positive）

```
cinematic, film still, in the style of MatthewBarney, 行为艺术影像、身体雕塑、极端美学、悬丝系列, 肉体粉色, 医学蓝白, 生物形态色, 身体雕塑, 装置影像, 身体政治 atmosphere, 工作室布光、雕塑式照明、冷色工业光、生物色光, 35mm, film grain, depth of field, masterpiece, best quality
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
- **触发词**：`in the style of MatthewBarney`
