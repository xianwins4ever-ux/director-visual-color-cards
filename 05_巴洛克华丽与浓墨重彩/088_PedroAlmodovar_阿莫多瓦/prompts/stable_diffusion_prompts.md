# 阿莫多瓦 — Stable Diffusion 提示词

> 风格：阿莫多瓦红、高饱和室内、西语热烈、女性视角

---

## 正向提示词（通用）

```
masterpiece, best quality, cinematic, film still, in the style of PedroAlmodovar,
阿莫多瓦红、高饱和室内、西语热烈、女性视角,
阿莫多瓦红, 高饱和室内, 西班牙色彩, 女性视角色,
女性群像, 室内空间, 色彩构图,
女性力量 atmosphere, 家庭秘密,
饱和色光、室内暖光、色彩分层、自然柔光,
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
- **触发词**：`pedroalmodovar_style`
- **训练步数**：3000-5000 步
- **重点标签**：色彩、装饰、光影
