# 约翰·布尔曼 — Stable Diffusion 提示词

> 风格：丛林神话、绿色饱和、自然原力、亚瑟王传说

---

## 正向提示词（Positive）

```
cinematic, film still, in the style of JohnBoorman, 丛林神话、绿色饱和、自然原力、亚瑟王传说, 丛林翠绿, 圣剑金光, 湖水深蓝, 丛林穿越, 亚瑟王传奇, 神话史诗 atmosphere, 森林光斑、水光反射、黄金时刻、神秘侧光, 35mm, film grain, depth of field, masterpiece, best quality
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
- **触发词**：`in the style of JohnBoorman`
