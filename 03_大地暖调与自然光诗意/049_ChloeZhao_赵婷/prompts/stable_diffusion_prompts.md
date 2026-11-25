# Stable Diffusion 提示词模板 — Chloé Zhao 赵婷风格

---

## 风格触发词
`Chloe Zhao style, nomadland aesthetic, natural magic hour lighting, dusty earth color palette, cinematic film still`

## 正向提示词
```
masterpiece, best quality, ultra detailed, 8k, photorealistic,
cinematic film still, in the style of Chloe Zhao,
nomadland aesthetic, natural magic hour light,
dusty earth color palette, desert golden hour,
sagebrush green, prairie wheat yellow, muted skin tone,
wide open landscape, horizon composition,
quiet human dignity, meditative stillness,
shallow depth of field, dust motes in sunlight,
static long take composition, film grain, naturalistic
```

## 反向提示词
```
(worst quality, low quality:1.4), studio lighting,
bright saturated colors, dramatic hollywood lighting,
glossy commercial look, 3d render, cartoon, anime,
fast action scene, overexposed, deformed, text, watermark,
clean sterile environment, perfect makeup
```

## ControlNet推荐
| 效果 | 模型 | 强度 |
|------|------|------|
| 风景构图 | Canny/LineArt | 0.7-0.9 |
| 光线 | Depth+IP-Adapter | 0.6-0.8 |
| 色彩 | IP-Adapter(电影截图) | 0.5-0.7 |
| 人像 | ControlNet OpenPose | 0.7-0.8 |

## 采样参数
Steps:30-40, CFG:6-9, Sampler:DPM++ 2M Karras, 分辨率:1536x1024 (风景) 或 1024x1536 (肖像)
