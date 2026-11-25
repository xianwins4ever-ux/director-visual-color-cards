# 阿彼察邦 — Stable Diffusion 提示词

> 风格：热带丛林、记忆梦境、慢长镜头、超自然日常

---

## 正向提示词（Positive）

```
cinematic, film still, in the style of ApichatpongWeerasethakul, 热带丛林、记忆梦境、慢长镜头、超自然日常, 阿彼察邦绿, 热带丛林色, 记忆暖金色, 热带丛林, 慢长镜头, 热带迷梦 atmosphere, 丛林绿光、热带柔光、自然天光、室内暖光, 35mm, film grain, depth of field, masterpiece, best quality
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
- **触发词**：`in the style of ApichatpongWeerasethakul`
