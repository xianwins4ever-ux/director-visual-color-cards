# 兰斯莫斯 — Stable Diffusion 提示词

> 风格：鱼眼广角、烛光古典、畸变华丽、荒诞礼仪

---

## 正向提示词（通用）

```
masterpiece, best quality, cinematic, film still, in the style of YorgosLanthimos,
鱼眼广角、烛光古典、畸变华丽、荒诞礼仪,
烛光暖调, 古典油画色, 鱼眼畸变色, 自然绿灰,
鱼眼广角, 畸变构图, 古典宫廷,
荒诞主义 atmosphere, 社会规训,
烛光照明、自然窗光、低照度室内、冷调户外,
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
- **触发词**：`yorgoslanthimos_style`
- **训练步数**：3000-5000 步
- **重点标签**：色彩、装饰、光影
