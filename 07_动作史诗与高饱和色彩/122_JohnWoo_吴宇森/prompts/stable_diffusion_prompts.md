# 吴宇森 — Stable Diffusion 提示词

> 风格：白鸽枪战、双枪慢镜、英雄血色、教堂仪式

---

## 正向提示词（Positive）

```
cinematic, film still, in the style of JohnWoo, 白鸽枪战、双枪慢镜、英雄血色、教堂仪式, 英雄血色, 教堂圣光, 夜色蓝紫, 双枪对峙, 白鸽慢镜, 英雄本色 atmosphere, 教堂彩光、霓虹夜色、火焰逆光、慢镜光斑, 35mm, film grain, depth of field, masterpiece, best quality
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
- **触发词**：`in the style of JohnWoo`
