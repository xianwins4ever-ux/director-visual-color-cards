# 温特伯格 — Stable Diffusion 提示词

> 风格：Dogme纪实、丹麦冷灰、手持亲密、群体压力

---

## 正向提示词（通用）

```
masterpiece, best quality, cinematic, film still, in the style of ThomasVinterberg,
Dogme纪实、丹麦冷灰、手持亲密、群体压力,
丹麦冷调, Dogme质感, 自然光, 室内暖光,
手持跟拍, 室内空间, 家庭聚会,
道德困境 atmosphere, 群体压力,
自然光为主、室内暖光、手持跟拍、去装饰,
35mm film, film grain, grainy, muted colors, desaturated,
cinematic composition, rule of thirds, depth of field
```

## 反向提示词

```
bright, vibrant colors, high saturation, cartoon, anime, illustration, 3d render,
overexposed, blown out highlights, hdr, unrealistic, perfect skin, smooth,
text, watermark, logo, frame, border,
modern, clean, polished, glossy
```

---

## ControlNet 建议

| 类型 | 强度 | 用途 |
|------|------|------|
| Canny | 0.5-0.7 | 保持构图线条 |
| Depth | 0.6-0.8 | 保持空间纵深 |
| Line Art | 0.4-0.6 | 保持画面结构 |
| OpenPose | 0.7-0.9 | 人物姿态控制 |

---

## LoRA 训练建议

- **推荐模型**：SD 1.5 / SDXL
- **训练图片**：20-30 张代表性电影截图
- **触发词**：`thomasvinterberg_style`
- **训练步数**：2000-4000 步
- **重点标签**：色彩、构图、光影
