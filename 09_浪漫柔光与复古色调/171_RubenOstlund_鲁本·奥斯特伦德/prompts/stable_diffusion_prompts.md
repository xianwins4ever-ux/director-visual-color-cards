# 鲁本·奥斯特伦德 — Stable Diffusion 提示词

> 风格：北欧冷色、阶级讽刺、长镜头观察、尴尬美学

---

## 正向提示词（Positive）

```
cinematic, film still, in the style of RubenOstlund, 北欧冷色、阶级讽刺、长镜头观察、尴尬美学, 北欧冷灰, 雪国白色, 奥斯特伦德冷调, 长镜头观察, 阶级讽刺, 阶级批判 atmosphere, 北欧冷光、自然散射光、雪国白光、博物馆光, 35mm, film grain, depth of field, masterpiece, best quality
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
- **触发词**：`in the style of RubenOstlund`
