# Stable Diffusion 提示词模板 — 迈克尔·曼 Michael Mann风格

---

## 风格触发词
`michael_mann style, Michael Mann film aesthetic, professional criminals, cinematic film still`

## 正向提示词
```
masterpiece, best quality, ultra detailed, 8k,
cinematic film still, in the style of Michael Mann,
digital cold blue, steel grey urban,
digital cinematography, digital cold blue night, practical sources, tungsten warm accents,
professional criminals, existential male loneliness atmosphere,
cinematic lighting, film grain, depth of field
```

## 反向提示词
```
(worst quality, low quality:1.4), bright daylight, cheerful mood,
flat lighting, cartoon, anime, 3d render, clean sterile look,
overexposed, blurry, deformed, text, watermark
```

## ControlNet推荐
| 效果 | 模型 | 强度 |
|------|------|------|
| 构图 | Canny/LineArt | 0.7-0.9 |
| 光线 | Depth+IP-Adapter | 0.6-0.8 |
| 色彩 | IP-Adapter(电影截图) | 0.5-0.7 |

## 采样参数
Steps:30-40, CFG:6-9, Sampler:DPM++ 2M Karras, 分辨率:1536x1024
