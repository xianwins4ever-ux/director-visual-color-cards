# 小津安二郎 — Stable Diffusion 提示词

> 风格：低角度榻榻米、固定镜头、禅意留白、茶碗日常

---

## 正向提示词（Positive）

```
cinematic, film still, in the style of YasujiroOzu, 低角度榻榻米、固定镜头、禅意留白、茶碗日常, 小津棕米, 和纸暖调, 禅意留白色, 低角度固定镜头, 榻榻米构图, 禅意日常 atmosphere, 室内柔光、窗格光影、纸灯笼暖光、自然天光, 35mm, film grain, depth of field, masterpiece, best quality
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
- **触发词**：`in the style of YasujiroOzu`
