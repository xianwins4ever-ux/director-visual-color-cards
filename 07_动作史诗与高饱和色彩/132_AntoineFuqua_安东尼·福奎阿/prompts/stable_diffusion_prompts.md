# 安东尼·福奎阿 — Stable Diffusion 提示词

> 风格：硬汉动作、蓝灰冷调、训练日美学、黑帮真实

---

## 正向提示词（Positive）

```
cinematic, film still, in the style of AntoineFuqua, 硬汉动作、蓝灰冷调、训练日美学、黑帮真实, 训练日蓝调, 街头真实色, 硬汉冷调, 硬汉主角, 街头真实, 硬汉动作 atmosphere, 硬光侧光、冷蓝夜色、暖黄室内、高对比阴影, 35mm, film grain, depth of field, masterpiece, best quality
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
- **触发词**：`in the style of AntoineFuqua`
