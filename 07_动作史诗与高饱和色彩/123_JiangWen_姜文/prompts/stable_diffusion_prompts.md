# 姜文 — Stable Diffusion 提示词

> 风格：雄性荷尔蒙、高饱和暖红、黄土大地、荒诞史诗

---

## 正向提示词（Positive）

```
cinematic, film still, in the style of JiangWen, 雄性荷尔蒙、高饱和暖红、黄土大地、荒诞史诗, 中国红, 黄土高原色, 高饱和暖调, 雄性群像, 黄土大地, 雄性荷尔蒙 atmosphere, 强烈侧光、暖红顶光、黄土漫反射、阳光硬光, 35mm, film grain, depth of field, masterpiece, best quality
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
- **触发词**：`in the style of JiangWen`
