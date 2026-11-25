# 彼得·格林纳威 — Stable Diffusion 提示词

> 风格：油画构图、红白绿分章、巴洛克对称、数字游戏

---

## 正向提示词（通用）

```
masterpiece, best quality, cinematic, film still, in the style of PeterGreenaway,
油画构图、红白绿分章、巴洛克对称、数字游戏,
高饱和三原色, 油画质感, 红绿对比, 金色装饰,
对称构图, 数字分章, 画框嵌套,
智性游戏 atmosphere, 巴洛克华丽,
舞台式布光、高饱和色光、对称照明、建筑投影,
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
- **触发词**：`petergreenaway_style`
- **训练步数**：3000-5000 步
- **重点标签**：色彩、装饰、光影
