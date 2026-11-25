# 巴兹·鲁赫曼 — Stable Diffusion 提示词

> 风格：极饱和金红、华丽运动、maximalism、MTV剪辑

---

## 正向提示词（通用）

```
masterpiece, best quality, cinematic, film still, in the style of BazLuhrmann,
极饱和金红、华丽运动、maximalism、MTV剪辑,
极饱和色彩, 金红华丽, 霓虹混色, 装饰艺术,
MTV式剪辑, 快速运动镜头, 舞台式场面,
狂欢悲剧 atmosphere, 浪漫极致,
高饱和色光、频闪运动、舞台聚光、霓虹混合,
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
- **触发词**：`bazluhrmann_style`
- **训练步数**：3000-5000 步
- **重点标签**：色彩、装饰、光影
