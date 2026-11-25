# 布里兰特·门多萨 — Stable Diffusion 提示词

> 风格：马尼拉贫民窟、手持纪实、社会暴力、真实质感

---

## 正向提示词（Positive）

```
cinematic, film still, in the style of BrillanteMendoza, 马尼拉贫民窟、手持纪实、社会暴力、真实质感, 门多萨灰棕, 菲律宾贫民窟色, 手持纪实色, 手持纪实, 马尼拉贫民窟, 社会批判 atmosphere, 自然光效、荧光冷光、街头灯光、暗调阴影, 35mm, film grain, depth of field, masterpiece, best quality
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
- **触发词**：`in the style of BrillanteMendoza`
