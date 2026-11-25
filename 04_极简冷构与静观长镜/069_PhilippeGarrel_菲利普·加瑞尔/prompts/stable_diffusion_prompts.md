# 菲利普·加瑞尔 — Stable Diffusion 提示词

> 风格：黑白亲密、60年代余韵、巴黎冷调、爱情哲学

---

## 正向提示词（通用）

```
masterpiece, best quality, cinematic, film still, in the style of PhilippeGarrel,
黑白亲密、60年代余韵、巴黎冷调、爱情哲学,
高反差黑白, 60年代质感, 巴黎灰调, 室内光影,
黑白影像, 室内对话, 巴黎公寓,
爱情哲学 atmosphere, 艺术家困境,
高反差黑白、窗光侧照、室内柔光、巴黎街灯,
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
- **触发词**：`philippegarrel_style`
- **训练步数**：2000-4000 步
- **重点标签**：色彩、构图、光影
