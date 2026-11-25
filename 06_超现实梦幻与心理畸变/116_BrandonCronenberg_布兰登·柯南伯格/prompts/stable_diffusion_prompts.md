# 布兰登·柯南伯格 — Stable Diffusion 提示词

> 风格：科幻肉体、数码畸变、冷色恐怖、身体政治

---

## 正向提示词（Positive）

```
cinematic, film still, in the style of BrandonCronenberg, 科幻肉体、数码畸变、冷色恐怖、身体政治, 临床冷白, 肉体粉红, 科幻恐怖色, 身体变形, 临床空间, 身体恐怖 atmosphere, 冷白荧光、肉色暖光、数码色光、临床照明, 35mm, film grain, depth of field, masterpiece, best quality
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
- **触发词**：`in the style of BrandonCronenberg`
