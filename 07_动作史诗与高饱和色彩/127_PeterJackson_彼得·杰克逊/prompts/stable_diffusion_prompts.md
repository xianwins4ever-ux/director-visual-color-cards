# 彼得·杰克逊 — Stable Diffusion 提示词

> 风格：中土史诗、新西兰地貌、魔幻金色、战争大场面

---

## 正向提示词（Positive）

```
cinematic, film still, in the style of PeterJackson, 中土史诗、新西兰地貌、魔幻金色、战争大场面, 魔戒金色, 中土大地色, 精灵绿色, 新西兰地貌, 大场面战争, 史诗魔幻 atmosphere, 魔幻金光、战场火光、洞穴暗影、自然天光, 35mm, film grain, depth of field, masterpiece, best quality
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
- **触发词**：`in the style of PeterJackson`
