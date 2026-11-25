# 让-吕克·戈达尔 — Stable Diffusion 提示词

> 风格：跳切革命、政治宣言、拼贴美学、电影史

---

## 正向提示词（Positive）

```
cinematic, film still, in the style of Jean-LucGodard, 跳切革命、政治宣言、拼贴美学、电影史, 戈达尔三原色, 革命红蓝白, 拼贴色块, 跳切剪辑, 直视镜头, 革命美学 atmosphere, 街头自然光、高对比黑白、彩色色块、实验光效, 35mm, film grain, depth of field, masterpiece, best quality
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
- **触发词**：`in the style of Jean-LucGodard`
