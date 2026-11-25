# 埃里克·侯麦 — Stable Diffusion 提示词

> 风格：自然光、对话哲学、四季色彩、道德故事

---

## 正向提示词（Positive）

```
cinematic, film still, in the style of EricRohmer, 自然光、对话哲学、四季色彩、道德故事, 侯麦四季色, 自然光效, 法国乡村色, 对话场景, 四季自然, 对话哲学 atmosphere, 自然柔光、窗光漫射、阳光斑驳、真实色彩, 35mm, film grain, depth of field, masterpiece, best quality
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
- **触发词**：`in the style of EricRohmer`
