# 雅克·德米 — Stable Diffusion 提示词

> 风格：歌舞童话、粉蓝浪漫、南特港口、雨伞店

---

## 正向提示词（Positive）

```
cinematic, film still, in the style of JacquesDemy, 歌舞童话、粉蓝浪漫、南特港口、雨伞店, 雅克德米粉蓝, 雨伞店蓝色, 罗什福尔粉, 歌舞场面, 南特港口, 浪漫歌舞 atmosphere, 童话柔光、粉蓝彩色、港口阳光、舞台式布光, 35mm, film grain, depth of field, masterpiece, best quality
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
- **触发词**：`in the style of JacquesDemy`
