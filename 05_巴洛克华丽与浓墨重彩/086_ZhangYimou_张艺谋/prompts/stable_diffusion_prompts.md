# 张艺谋 — Stable Diffusion 提示词

> 风格：中国红黄、大面积纯色、对称仪式、民俗浓烈

---

## 正向提示词（通用）

```
masterpiece, best quality, cinematic, film still, in the style of ZhangYimou,
中国红黄、大面积纯色、对称仪式、民俗浓烈,
中国红黄, 高饱和纯色, 民俗色彩, 灯笼暖光,
对称构图, 大面积纯色, 民俗仪式,
民族史诗 atmosphere, 命运抗争,
高饱和纯色光、对称照明、灯笼暖光、自然硬光,
35mm film, film grain, grainy, rich colors, baroque, ornate,
cinematic composition, rule of thirds, depth of field, dramatic lighting
```

## 反向提示词

```
bright, pastel colors, low saturation, cartoon, anime, illustration, 3d render,
overexposed, modern, clean, minimal,
text, watermark, logo, frame, border,
flat lighting, low contrast, washed out
```

---

## ControlNet 建议

| 类型 | 强度 | 用途 |
|------|------|------|
| Canny | 0.6-0.8 | 保持华丽线条 |
| Depth | 0.7-0.9 | 保持空间纵深 |
| Line Art | 0.5-0.7 | 保持装饰细节 |
| OpenPose | 0.7-0.9 | 人物姿态控制 |

---

## LoRA 训练建议

- **推荐模型**：SD 1.5 / SDXL
- **训练图片**：20-30 张代表性电影截图
- **触发词**：`zhangyimou_style`
- **训练步数**：3000-5000 步
- **重点标签**：色彩、装饰、光影
