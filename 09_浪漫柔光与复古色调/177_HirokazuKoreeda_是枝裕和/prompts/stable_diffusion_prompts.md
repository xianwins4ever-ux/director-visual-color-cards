# 是枝裕和 — Stable Diffusion 提示词

> 风格：家庭温情、夏日绿调、静水流深、庶民剧

---

## 正向提示词（Positive）

```
cinematic, film still, in the style of HirokazuKoreeda, 家庭温情、夏日绿调、静水流深、庶民剧, 是枝裕和绿, 家庭暖调, 夏日绿蓝, 家庭群像, 夏日风景, 家庭温情 atmosphere, 自然柔光、夏日绿意、室内暖光、真实质感, 35mm, film grain, depth of field, masterpiece, best quality
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
- **触发词**：`in the style of HirokazuKoreeda`
