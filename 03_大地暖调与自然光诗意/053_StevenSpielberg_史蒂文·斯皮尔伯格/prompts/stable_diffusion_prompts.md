# Stable Diffusion 提示词模板 — Steven Spielberg 史蒂文·斯皮尔伯格风格

---

## 风格触发词
`Steven Spielberg style, cinematic backlit silhouette, warm golden rim light, teal and orange epic palette, hollywood epic film still`

## 正向提示词
```
masterpiece, best quality, ultra detailed, 8k, photorealistic,
cinematic film still, in the style of Steven Spielberg,
backlit silhouette, warm golden hour rim light,
teal and orange epic palette, golden hour magic light,
dust motes in light beam, anamorphic lens flares,
hollywood epic grandeur, sense of wonder and awe,
low angle shot, fog and haze atmosphere,
dolly zoom or tracking shot composition,
film grain, anamorphic wide, high contrast
```

## 反向提示词
```
(worst quality, low quality:1.4), flat lighting,
modern digital look, cartoon, anime, 3d render,
comedy vibe, shallow theme, overexposed,
deformed, text, watermark, low budget feel
```

## ControlNet推荐
| 效果 | 模型 | 强度 |
|------|------|------|
| 构图 | Canny/LineArt | 0.7-0.9 |
| 光线 | Depth+IP-Adapter | 0.6-0.8 |
| 色彩 | IP-Adapter(电影截图) | 0.5-0.7 |
| 景深 | ControlNet Depth | 0.6-0.8 |

## 采样参数
Steps:30-40, CFG:7-10, Sampler:DPM++ 2M Karras, 分辨率:1792x1024 (宽幅) 或 1536x1024 (标准)
