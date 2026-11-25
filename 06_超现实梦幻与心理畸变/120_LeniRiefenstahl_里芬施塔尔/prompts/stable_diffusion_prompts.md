# 里芬施塔尔 — Stable Diffusion 提示词

> 风格：壮美构图、人体雕塑光、史诗光影、山岳美学

---

## 正向提示词（Positive）

```
cinematic, film still, in the style of LeniRiefenstahl, 壮美构图、人体雕塑光、史诗光影、山岳美学, 壮美金色, 山岳蓝白, 雕塑光感, 对称壮美, 人体雕塑, 壮美美学 atmosphere, 侧光雕刻、阳光塑形、云雾光束、舞台式布光, 35mm, film grain, depth of field, masterpiece, best quality
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
- **触发词**：`in the style of LeniRiefenstahl`
