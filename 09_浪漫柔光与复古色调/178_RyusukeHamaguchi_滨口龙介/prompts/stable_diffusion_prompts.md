# 滨口龙介 — Stable Diffusion 提示词

> 风格：对话长镜、偶然想象、日常魔幻、三轮春生

---

## 正向提示词（Positive）

```
cinematic, film still, in the style of RyusukeHamaguchi, 对话长镜、偶然想象、日常魔幻、三轮春生, 滨口龙介蓝绿, 日常对话色, 偶然与想象色, 对话长镜, 日常空间, 对话电影 atmosphere, 自然光效、室内柔光、窗外景色、真实质感, 35mm, film grain, depth of field, masterpiece, best quality
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
- **触发词**：`in the style of RyusukeHamaguchi`
