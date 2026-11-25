# Stable Diffusion 提示词模板 — Sean Baker 肖恩·贝克风格

---

## 风格触发词
`Sean Baker style, florida project aesthetic, iPhone cinematography, handheld vérité, saturated warm orange palette, cinematic film still`

## 正向提示词
```
masterpiece, best quality, ultra detailed, 8k, photorealistic,
cinematic film still, in the style of Sean Baker,
florida project aesthetic, iPhone cinematography,
harsh daylight sun, saturated warm orange palette,
neon pink motel, florida orange, sunset coral pink,
trans skin warmth, fast food yellow, dusk purple sky,
handheld vérité, street-level framing,
marginal lives humanity, working class warmth,
anamorphic wide frame, film grain, naturalistic
```

## 反向提示词
```
(worst quality, low quality:1.4), studio lighting,
soft glow, hollywood glamour, perfect makeup,
wealthy setting, clean pristine environment,
3d render, cartoon, anime, soft focus,
overexposed, deformed, text, watermark,
luxury aesthetic, upscale neighborhood
```

## ControlNet推荐
| 效果 | 模型 | 强度 |
|------|------|------|
| 街头构图 | Canny/LineArt | 0.7-0.9 |
| 光线 | Depth+IP-Adapter | 0.6-0.8 |
| 色彩 | IP-Adapter(电影截图) | 0.5-0.7 |
| 人物姿态 | ControlNet OpenPose | 0.7-0.8 |

## 采样参数
Steps:30-40, CFG:6-9, Sampler:DPM++ 2M Karras, 分辨率:1536x1024 (横幅) 或 1792x1024 (宽幅)
