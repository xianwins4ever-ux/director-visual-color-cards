# 米林宏昌 — Stable Diffusion 提示词

> 风格：吉卜力传承、小人视角、细腻手绘、温暖奇幻

---

## 正向提示词（Positive）

```
cinematic, film still, in the style of HiromasaYonebayashi, 吉卜力传承、小人视角、细腻手绘、温暖奇幻, 吉卜力绿, 小人视角色彩, 森林暖调, 小人视角, 微观世界, 吉卜力传承 atmosphere, 森林柔光、室内暖光、自然天光、夕阳金辉, 35mm, film grain, depth of field, masterpiece, best quality
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
- **触发词**：`in the style of HiromasaYonebayashi`
