# 希尔万·肖梅 — Stable Diffusion 提示词

> 风格：法式怀旧、水彩插画、音乐叙事、温情默片

---

## 正向提示词（Positive）

```
cinematic, film still, in the style of SylvainChomet, 法式怀旧、水彩插画、音乐叙事、温情默片, 法式怀旧色, 水彩插画色, 暖黄街灯色, 法式街景, 水彩插画, 法式温情 atmosphere, 暖黄街灯、雨天柔光、室内暖光、夕阳光辉, 35mm, film grain, depth of field, masterpiece, best quality
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
- **触发词**：`in the style of SylvainChomet`
