# 库斯图里卡 — Stable Diffusion 提示词

> 风格：吉普赛狂欢、铜管暖色、巴尔干热烈、魔幻现实

---

## 正向提示词（Positive）

```
cinematic, film still, in the style of EmirKusturica, 吉普赛狂欢、铜管暖色、巴尔干热烈、魔幻现实, 巴尔干暖色, 吉普赛色彩, 火焰橙黄, 狂欢场面, 铜管乐队, 狂欢悲剧 atmosphere, 暖金火光、节日灯彩、自然阳光、室内暖光, 35mm, film grain, depth of field, masterpiece, best quality
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
- **触发词**：`in the style of EmirKusturica`
