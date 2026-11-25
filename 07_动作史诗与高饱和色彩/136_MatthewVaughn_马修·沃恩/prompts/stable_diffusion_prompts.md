# 马修·沃恩 — Stable Diffusion 提示词

> 风格：英式酷感、高饱和漫画风、暴力美学、 Kingsman西装

---

## 正向提示词（Positive）

```
cinematic, film still, in the style of MatthewVaughn, 英式酷感、高饱和漫画风、暴力美学、 Kingsman西装, 金士曼蓝金, 西装色调, 漫画风高饱和, 漫画分镜, 西装动作, 绅士特工 atmosphere, 漫画色光、西装冷光、动作补光、高对比色, 35mm, film grain, depth of field, masterpiece, best quality
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
- **触发词**：`in the style of MatthewVaughn`
