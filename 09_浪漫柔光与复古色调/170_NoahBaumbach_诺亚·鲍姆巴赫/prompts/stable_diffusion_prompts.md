# 诺亚·鲍姆巴赫 — Stable Diffusion 提示词

> 风格：纽约知识分子、家庭对话、黑白彩色、散文电影

---

## 正向提示词（Positive）

```
cinematic, film still, in the style of NoahBaumbach, 纽约知识分子、家庭对话、黑白彩色、散文电影, 鲍姆巴赫暖调, 纽约知识分子色, 家庭对话色, 纽约公寓, 家庭对话, 知识分子 atmosphere, 纽约自然光、室内暖光、黑白高对比、柔光漫射, 35mm, film grain, depth of field, masterpiece, best quality
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
- **触发词**：`in the style of NoahBaumbach`
