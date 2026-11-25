# Stable Diffusion 提示词模板 — Ken Loach 肯·洛奇风格

---

## 风格触发词
`Ken Loach style, british social realism, documentary naturalism, overcast natural light, muted earth palette, cinematic film still`

## 正向提示词
```
masterpiece, best quality, ultra detailed, 8k, photorealistic,
cinematic film still, in the style of Ken Loach,
british social realism, documentary naturalism,
overcast natural light, soft window light,
muted grey-blue and warm earth palette,
british council grey, irish countryside green,
weathered wood brown, stone wall beige,
static medium shot, working class setting,
humanistic socialist cinema, quiet dignity,
shallow depth of field, film grain, natural flat lighting
```

## 反向提示词
```
(worst quality, low quality:1.4), dramatic lighting,
hollywood style, highly saturated colors,
hero shot, low angle power shot, 3d render,
cartoon, anime, wealthy setting, luxury,
studio lighting, overexposed, deformed, text, watermark
```

## ControlNet推荐
| 效果 | 模型 | 强度 |
|------|------|------|
| 构图 | Canny/LineArt | 0.7-0.9 |
| 光线 | Depth+IP-Adapter | 0.6-0.8 |
| 色彩 | IP-Adapter(电影截图) | 0.5-0.7 |
| 群像 | ControlNet OpenPose | 0.7-0.8 |

## 采样参数
Steps:30-40, CFG:6-9, Sampler:DPM++ 2M Karras, 分辨率:1024x1280 (竖幅) 或 1536x1024 (横幅)
