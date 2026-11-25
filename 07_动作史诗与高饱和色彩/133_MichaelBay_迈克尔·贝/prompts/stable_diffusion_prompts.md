# 迈克尔·贝 — Stable Diffusion 提示词

> 风格：爆炸美学、360°环绕、橙蓝高饱和、慢动作爆炸

---

## 正向提示词（Positive）

```
cinematic, film still, in the style of MichaelBay, 爆炸美学、360°环绕、橙蓝高饱和、慢动作爆炸, 贝式橙蓝, 爆炸高饱和, 黄金时刻光, 360°环绕, 慢动作爆炸, 爆炸美学 atmosphere, 爆炸逆光、黄金时刻、高对比暖光、直升机光, 35mm, film grain, depth of field, masterpiece, best quality
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
- **触发词**：`in the style of MichaelBay`
