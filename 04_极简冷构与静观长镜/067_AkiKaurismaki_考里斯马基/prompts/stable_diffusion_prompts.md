# 考里斯马基 — Stable Diffusion 提示词

> 风格：极简冷面、复古低饱和、工人蓝灰、静默幽默

---

## 正向提示词（通用）

```
masterpiece, best quality, cinematic, film still, in the style of AkiKaurismaki,
极简冷面、复古低饱和、工人蓝灰、静默幽默,
低饱和蓝, 复古色调, 工人阶级色, 芬兰冷调,
对称构图, 平面感, 复古影棚,
冷面幽默 atmosphere, 工人诗意,
柔光平光、复古影棚光、冷色调为主、暖色点缀,
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
- **触发词**：`akikaurismaki_style`
- **训练步数**：2000-4000 步
- **重点标签**：色彩、构图、光影
