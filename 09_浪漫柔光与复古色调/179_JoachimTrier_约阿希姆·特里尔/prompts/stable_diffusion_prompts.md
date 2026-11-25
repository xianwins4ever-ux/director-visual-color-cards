# 约阿希姆·特里尔 — Stable Diffusion 提示词

> 风格：奥斯陆三部曲、北欧冷光、内心独白、青春回忆

---

## 正向提示词（Positive）

```
cinematic, film still, in the style of JoachimTrier, 奥斯陆三部曲、北欧冷光、内心独白、青春回忆, 奥斯陆灰蓝, 北欧冷调, 青春暖黄, 奥斯陆风景, 内心独白, 奥斯陆三部曲 atmosphere, 北欧冷光、奥斯陆冬光、室内暖光、自然散射, 35mm, film grain, depth of field, masterpiece, best quality
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
- **触发词**：`in the style of JoachimTrier`
