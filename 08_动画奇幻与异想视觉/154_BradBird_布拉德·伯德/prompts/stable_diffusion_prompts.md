# 布拉德·伯德 — Stable Diffusion 提示词

> 风格：复古未来主义、超人家庭、黄金时代动画、动作流畅

---

## 正向提示词（Positive）

```
cinematic, film still, in the style of BradBird, 复古未来主义、超人家庭、黄金时代动画、动作流畅, 超人红蓝, 复古未来色, 50年代暖调, 复古未来, 超人家庭, 英雄主义 atmosphere, 复古暖光、金属冷光、50年代色、高对比动作光, 35mm, film grain, depth of field, masterpiece, best quality
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
- **触发词**：`in the style of BradBird`
