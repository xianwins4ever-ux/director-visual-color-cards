# 安德鲁·斯坦顿 — Stable Diffusion 提示词

> 风格：皮克斯史诗、海洋深邃、科幻冒险、情感深度

---

## 正向提示词（Positive）

```
cinematic, film still, in the style of AndrewStanton, 皮克斯史诗、海洋深邃、科幻冒险、情感深度, 海底蓝绿, 瓦力橙蓝, 皮克斯史诗色, 海底世界, 太空史诗, 史诗冒险 atmosphere, 海底柔光、太空冷光、沙漠暖光、自然天光, 35mm, film grain, depth of field, masterpiece, best quality
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
- **触发词**：`in the style of AndrewStanton`
