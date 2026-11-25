# 哈蒙尼·科林 — Stable Diffusion 提示词

> 风格：迷幻青春、VHS美学、霓虹垃圾、边缘狂欢

---

## 正向提示词（Positive）

```
cinematic, film still, in the style of HarmonyKorine, 迷幻青春、VHS美学、霓虹垃圾、边缘狂欢, VHS迷幻色, 霓虹粉青, 青春堕落色, VHS质感, 手持混乱, 迷幻青春 atmosphere, 霓虹色光、VHS噪点、日光直射、派对彩光, 35mm, film grain, depth of field, masterpiece, best quality
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
- **触发词**：`in the style of HarmonyKorine`
