# Stable Diffusion 提示词模板 — Andrea Arnold 安德烈·阿诺德风格

---

## 风格触发词
`Andrea Arnold style, british social realism aesthetic, cinéma vérité, handheld natural light, cinematic film still`

## 正向提示词
```
masterpiece, best quality, ultra detailed, 8k, photorealistic,
cinematic film still, in the style of Andrea Arnold,
british social realism, handheld cinéma vérité,
golden hour amber glow, natural earth-tone color palette,
moorland heather green, council estate grey, skin tone warmth,
tight close-up intimacy, shallow depth of field,
working-class setting, raw youth vulnerability,
natural daylight, film grain, documentary feel
```

## 反向提示词
```
(worst quality, low quality:1.4), studio lighting,
glossy commercial look, perfect makeup, overly saturated colors,
steady tripod shot, 3d render, cartoon, anime,
clean sterile environment, hollywood glamour,
overexposed, deformed, text, watermark
```

## ControlNet推荐
| 效果 | 模型 | 强度 |
|------|------|------|
| 构图 | Canny/LineArt | 0.7-0.9 |
| 光线 | Depth+IP-Adapter | 0.6-0.8 |
| 色彩 | IP-Adapter(电影截图) | 0.5-0.7 |
| 真实感 | ControlNet Tile | 0.5-0.6 |

## 采样参数
Steps:30-40, CFG:6-9, Sampler:DPM++ 2M Karras, 分辨率:1024x1536 (竖幅) 或 1536x1024 (横幅)
