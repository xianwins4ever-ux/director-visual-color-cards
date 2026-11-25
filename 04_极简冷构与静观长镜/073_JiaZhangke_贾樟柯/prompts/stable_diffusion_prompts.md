# 贾樟柯 — Stable Diffusion 提示词

> 风格：县城灰蓝、纪实与虚构、时代废墟、流行音乐

---

## 正向提示词（通用）

```
masterpiece, best quality, cinematic, film still, in the style of JiaZhangke,
县城灰蓝、纪实与虚构、时代废墟、流行音乐,
县城灰调, 黄土色, 汾阳旧色, 三峡绿,
县城空间, 长镜头静观, 流行音乐,
时代变迁 atmosphere, 乡愁,
自然光写实、县城灰蒙、霓虹夜色、室内暖光,
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
- **触发词**：`jiazhangke_style`
- **训练步数**：2000-4000 步
- **重点标签**：色彩、构图、光影
