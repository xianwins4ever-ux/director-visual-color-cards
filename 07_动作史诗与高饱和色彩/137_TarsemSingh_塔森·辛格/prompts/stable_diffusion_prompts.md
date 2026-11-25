# 塔森·辛格 — Stable Diffusion 提示词

> 风格：画框构图、极致美术、异域色彩、每一帧都是画

---

## 正向提示词（Positive）

```
cinematic, film still, in the style of TarsemSingh, 画框构图、极致美术、异域色彩、每一帧都是画, 印度异域色, 极致美术色彩, 画框式配色, 画框构图, 极致美术, 视觉盛宴 atmosphere, 画框式布光、彩色色光、自然天光、舞台式照明, 35mm, film grain, depth of field, masterpiece, best quality
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
- **触发词**：`in the style of TarsemSingh`
