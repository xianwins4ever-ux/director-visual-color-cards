# 科斯马托斯 — Stable Diffusion 提示词

> 风格：霓虹噩梦、合成器紫红、迷幻恐怖、慢镜暴力

---

## 正向提示词（Positive）

```
cinematic, film still, in the style of PanosCosmatos, 霓虹噩梦、合成器紫红、迷幻恐怖、慢镜暴力, 合成器紫, 霓虹粉蓝, 迷幻恐怖色, 合成器波美学, 慢镜暴力, 迷幻恐怖 atmosphere, 霓虹色光、合成器光感、红色点缀、暗调高对比, 35mm, film grain, depth of field, masterpiece, best quality
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
- **触发词**：`in the style of PanosCosmatos`
